---
title: Referência de API de utilitários de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601793"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="40bbc-103">Referência de API de utilitários de console</span><span class="sxs-lookup"><span data-stu-id="40bbc-103">Console Utilities API Reference</span></span>   



<span data-ttu-id="40bbc-104">A API de utilitários de console contém um conjunto de comandos de conveniência para realizar tarefas comuns: selecionando e inspecionando os elementos DOM, exibindo dados em um formato legível, interrompendo e iniciando o gerador de perfil e monitorando eventos DOM.</span><span class="sxs-lookup"><span data-stu-id="40bbc-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="40bbc-105">Os comandos a seguir só funcionam no console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="40bbc-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="40bbc-106">Os comandos não funcionam se forem executados a partir de seus scripts.</span><span class="sxs-lookup"><span data-stu-id="40bbc-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="40bbc-107">Procurando `console.log()` , `console.error()` e o restante dos `console.*` métodos?</span><span class="sxs-lookup"><span data-stu-id="40bbc-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="40bbc-108">Consulte [referência de API do console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="40bbc-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="40bbc-109">Expressão avaliada recentemente</span><span class="sxs-lookup"><span data-stu-id="40bbc-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="40bbc-110">Retorna o valor da expressão avaliada mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="40bbc-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="40bbc-111">Na [Figura 1](#figure-1), uma expressão simples \ ( `2 + 2` \) é avaliada.</span><span class="sxs-lookup"><span data-stu-id="40bbc-111">In [Figure 1](#figure-1), a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="40bbc-112">A `$_` propriedade é então avaliada, que contém o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="40bbc-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

> ##### <span data-ttu-id="40bbc-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="40bbc-113">Figure 1</span></span>  
> `$_` <span data-ttu-id="40bbc-114">é a expressão avaliada mais recentemente</span><span class="sxs-lookup"><span data-stu-id="40bbc-114">is the most recently evaluated expression</span></span>  
> ![$ _ é a expressão avaliada mais recentemente][ImageRecentExpression]  

<span data-ttu-id="40bbc-116">Na [Figura 2](#figure-2), a expressão avaliada inicialmente contém uma matriz de nomes.</span><span class="sxs-lookup"><span data-stu-id="40bbc-116">In [Figure 2](#figure-2), the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="40bbc-117">Avaliando `$_.length` para localizar o comprimento da matriz, o valor armazenado em `$_` alterações para se tornar a expressão avaliada mais recente `4` .</span><span class="sxs-lookup"><span data-stu-id="40bbc-117">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

> ##### <span data-ttu-id="40bbc-118">Figura 2</span><span class="sxs-lookup"><span data-stu-id="40bbc-118">Figure 2</span></span>  
> `$_` <span data-ttu-id="40bbc-119">alterações quando novos comandos são avaliados</span><span class="sxs-lookup"><span data-stu-id="40bbc-119">changes when new commands are evaluated</span></span>  
> ![$ _ muda quando novos comandos são avaliados][ImageChangedRecentExpression]  

## <span data-ttu-id="40bbc-121">Elemento ou objeto JavaScript selecionado recentemente</span><span class="sxs-lookup"><span data-stu-id="40bbc-121">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="40bbc-122">Retorna o elemento do elemento JavaScript ou o objeto selecionado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="40bbc-122">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="40bbc-123">Retorna a segunda opção selecionada mais recentemente e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="40bbc-123">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="40bbc-124">Os `$0` comandos,,, `$1` `$2` `$3` e `$4` funcionam como uma referência histórica aos cinco últimos elementos DOM inspecionados no painel **elementos** ou nos últimos cinco objetos de heap JavaScript selecionados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-124">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

<span data-ttu-id="40bbc-125">Na [Figura 3](#figure-3), um `img` elemento é selecionado no painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-125">In [Figure 3](#figure-3), an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="40bbc-126">Na gaveta do **console** , foi `$0` avaliada e exibe o mesmo elemento.</span><span class="sxs-lookup"><span data-stu-id="40bbc-126">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

> ##### <span data-ttu-id="40bbc-127">Figura 3</span><span class="sxs-lookup"><span data-stu-id="40bbc-127">Figure 3</span></span>  
> <span data-ttu-id="40bbc-128">O</span><span class="sxs-lookup"><span data-stu-id="40bbc-128">The</span></span> `$0`  
> ![O $0][ImageElement0]  

<span data-ttu-id="40bbc-130">Na [Figura 4](#figure-4), a imagem mostra um elemento diferente selecionado na mesma página.</span><span class="sxs-lookup"><span data-stu-id="40bbc-130">In [Figure 4](#figure-4), the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="40bbc-131">O `$0` agora se refere ao elemento selecionado recentemente, enquanto `$1` retorna o anterior selecionado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-131">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

> ##### <span data-ttu-id="40bbc-132">Figura 4</span><span class="sxs-lookup"><span data-stu-id="40bbc-132">Figure 4</span></span>  
> <span data-ttu-id="40bbc-133">O</span><span class="sxs-lookup"><span data-stu-id="40bbc-133">The</span></span> `$1`  
> ![O $1][ImageElement1]  

## <span data-ttu-id="40bbc-135">Seletor de consulta</span><span class="sxs-lookup"><span data-stu-id="40bbc-135">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="40bbc-136">Retorna a referência ao primeiro elemento DOM com o seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-136">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="40bbc-137">Esse método é um alias para o método [Document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="40bbc-137">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="40bbc-138">Na [Figura 5](#figure-5), uma referência para o primeiro `<img>` elemento no documento é retornada.</span><span class="sxs-lookup"><span data-stu-id="40bbc-138">In [Figure 5](#figure-5), a reference to the first `<img>` element in the document is returned.</span></span>  

> ##### <span data-ttu-id="40bbc-139">Figura 5</span><span class="sxs-lookup"><span data-stu-id="40bbc-139">Figure 5</span></span>  
> <span data-ttu-id="40bbc-140">O</span><span class="sxs-lookup"><span data-stu-id="40bbc-140">The</span></span> `$('img')`  
> ![$ (' Img ')][ImageElementImg]  

<span data-ttu-id="40bbc-142">Clique com o botão direito do mouse no resultado retornado e selecione **revelar no painel de elementos** para localizá-lo no dom ou **role para ver para exibi** -lo na página.</span><span class="sxs-lookup"><span data-stu-id="40bbc-142">Right-click on the returned result and select **Reveal in Elements Panel** to find it in the DOM, or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="40bbc-143">Na [Figura 6](#figure-6), uma referência ao elemento atualmente selecionado é retornada e a propriedade src é exibida.</span><span class="sxs-lookup"><span data-stu-id="40bbc-143">In [Figure 6](#figure-6), a reference to the currently selected element is returned and the src property is displayed.</span></span>  

> ##### <span data-ttu-id="40bbc-144">Figura 6</span><span class="sxs-lookup"><span data-stu-id="40bbc-144">Figure 6</span></span>  
> <span data-ttu-id="40bbc-145">O</span><span class="sxs-lookup"><span data-stu-id="40bbc-145">The</span></span> `$('img').src`  
> ![$ (' Img '). src][ImageElementImgSource]  

<span data-ttu-id="40bbc-147">Esse método também dá suporte a um segundo parâmetro, startNode, que especifica um "elemento" ou um nó do qual Pesquisar elementos.</span><span class="sxs-lookup"><span data-stu-id="40bbc-147">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="40bbc-148">O valor padrão desse parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="40bbc-148">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="40bbc-149">Na [Figura 7](#figure-7), o primeiro `img` elemento é encontrado após a `title--image` e exibe o valor `src` correto.</span><span class="sxs-lookup"><span data-stu-id="40bbc-149">In [Figure 7](#figure-7), the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

> ##### <span data-ttu-id="40bbc-150">Figura 7</span><span class="sxs-lookup"><span data-stu-id="40bbc-150">Figure 7</span></span>  
> <span data-ttu-id="40bbc-151">$ (' Img ', Document. querySelector (' título--imagem ')). src</span><span class="sxs-lookup"><span data-stu-id="40bbc-151">The $('img', document.querySelector('title--image')).src</span></span>  
> ![$ (' Img ', Document. querySelector (' título--imagem ')). src][ImageElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="40bbc-153">Se você estiver usando uma biblioteca como o jQuery que usa `$` , essa funcionalidade será sobrescrita e `$` corresponderá à implementação dessa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="40bbc-153">If you are using a library such as jQuery that uses `$`, this functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="40bbc-154">Seletor de consulta tudo</span><span class="sxs-lookup"><span data-stu-id="40bbc-154">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="40bbc-155">Retorna uma matriz de elementos que correspondem ao seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-155">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="40bbc-156">Esse método é equivalente a chamar o método [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="40bbc-156">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="40bbc-157">Na [Figura 8](#figure-8), use `$$()` para criar uma matriz de todos os `<img>` elementos no documento atual e exibir o valor da `src` propriedade de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="40bbc-157">In [Figure 8](#figure-8), use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="40bbc-158">Figura 8</span><span class="sxs-lookup"><span data-stu-id="40bbc-158">Figure 8</span></span>  
> <span data-ttu-id="40bbc-159">Usar `$$()` para selecionar todas as imagens no documento e exibir as fontes</span><span class="sxs-lookup"><span data-stu-id="40bbc-159">Using `$$()` to select all images in the document and display the sources</span></span>  
> ![Usando $ $ () para selecionar todas as imagens no documento e exibir as fontes][ImageArrayElementImgSource]  

<span data-ttu-id="40bbc-161">Esse método também oferece suporte a um segundo parâmetro, startNode, que especifica um elemento ou nó do qual Pesquisar elementos.</span><span class="sxs-lookup"><span data-stu-id="40bbc-161">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="40bbc-162">O valor padrão desse parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="40bbc-162">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="40bbc-163">Na [Figura 9](#figure-9), uma versão modificada da [Figura 8](#figure-8) usa `$$()` para criar uma matriz de todos os `<img>` elementos que aparecem no documento atual após o nó selecionado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-163">In [Figure 9](#figure-9), a modified version of [Figure 8](#figure-8) uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="40bbc-164">Figura 9</span><span class="sxs-lookup"><span data-stu-id="40bbc-164">Figure 9</span></span>  
> <span data-ttu-id="40bbc-165">Usar `$$()` para selecionar todas as imagens que aparecem após o `<div>` elemento especificado no documento e exibir as fontes</span><span class="sxs-lookup"><span data-stu-id="40bbc-165">Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
> ![Usando $ $ () para selecionar todas as imagens que aparecem após o <div especificado> o elemento no documento e exibir as fontes][ImageArrayElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="40bbc-167">Pressione `Shift` + `Enter` no console para iniciar uma nova linha sem executar o script.</span><span class="sxs-lookup"><span data-stu-id="40bbc-167">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="40bbc-168">XPath</span><span class="sxs-lookup"><span data-stu-id="40bbc-168">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="40bbc-169">Retorna uma matriz de elementos DOM que correspondem à expressão XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="40bbc-169">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="40bbc-170">Na [Figura 10](#figure-10), todos os `<p>` elementos na página são retornados.</span><span class="sxs-lookup"><span data-stu-id="40bbc-170">In [Figure 10](#figure-10), all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

> ##### <span data-ttu-id="40bbc-171">Figura 10</span><span class="sxs-lookup"><span data-stu-id="40bbc-171">Figure 10</span></span>  
> <span data-ttu-id="40bbc-172">Usando um seletor XPath</span><span class="sxs-lookup"><span data-stu-id="40bbc-172">Using an XPath selector</span></span>  
> ![Usando um seletor XPath][ImageArrayXpath]  

<span data-ttu-id="40bbc-174">Na [Figura 11](#figure-11), todos os `<p>` elementos que contêm `<a>` elementos são retornados.</span><span class="sxs-lookup"><span data-stu-id="40bbc-174">In [Figure 11](#figure-11), all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

> ##### <span data-ttu-id="40bbc-175">Figura 11</span><span class="sxs-lookup"><span data-stu-id="40bbc-175">Figure 11</span></span>  
> <span data-ttu-id="40bbc-176">Usando um seletor XPath mais complicado</span><span class="sxs-lookup"><span data-stu-id="40bbc-176">Using a more complicated XPath selector</span></span>  
> ![Usando um seletor XPath mais complicado][ImageArrayXpathChild]  

<span data-ttu-id="40bbc-178">Semelhante aos outros comandos do seletor, `$x(path)` tem um segundo parâmetro opcional, `startNode` que especifica um elemento ou nó do qual Pesquisar elementos.</span><span class="sxs-lookup"><span data-stu-id="40bbc-178">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

> ##### <span data-ttu-id="40bbc-179">Figura 12</span><span class="sxs-lookup"><span data-stu-id="40bbc-179">Figure 12</span></span>  
> <span data-ttu-id="40bbc-180">Usando um seletor XPath com</span><span class="sxs-lookup"><span data-stu-id="40bbc-180">Using an XPath selector with</span></span> `startNode`  
> ![Usando um seletor XPath com startNode][ImageArrayXpathNode]  

## <span data-ttu-id="40bbc-182">elimina</span><span class="sxs-lookup"><span data-stu-id="40bbc-182">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="40bbc-183">Limpa o console do histórico.</span><span class="sxs-lookup"><span data-stu-id="40bbc-183">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="40bbc-184">copy</span><span class="sxs-lookup"><span data-stu-id="40bbc-184">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="40bbc-185">O `copy(object)` método copia uma representação de cadeia de caracteres do objeto especificado para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="40bbc-185">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="40bbc-186">depurar</span><span class="sxs-lookup"><span data-stu-id="40bbc-186">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="40bbc-187">O [problema Chromium #1050237][MonorailIssue1050237] está acompanhando um bug com a `debug()` função.</span><span class="sxs-lookup"><span data-stu-id="40bbc-187">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="40bbc-188">Se você encontrar esse problema, tente [usar pontos de interrupção][DevtoolsJavascriptBreakpoints] em vez disso.</span><span class="sxs-lookup"><span data-stu-id="40bbc-188">If you encounter this issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="40bbc-189">Quando você solicita o método especificado, o depurador é invocado e é quebrado dentro do método no painel **fontes** , permitindo que você percorra o código e depure-o.</span><span class="sxs-lookup"><span data-stu-id="40bbc-189">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

> ##### <span data-ttu-id="40bbc-190">Figura 13</span><span class="sxs-lookup"><span data-stu-id="40bbc-190">Figure 13</span></span>  
> <span data-ttu-id="40bbc-191">Quebrando dentro de um método com</span><span class="sxs-lookup"><span data-stu-id="40bbc-191">Breaking inside a method with</span></span> `debug()`  
> ![Quebrando dentro de um método com debug ()][ImageDebugMethod]  

<span data-ttu-id="40bbc-193">Use `undebug(method)` para parar de quebrar o método ou use a interface do usuário para desativar todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="40bbc-193">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="40bbc-194">Para obter mais informações sobre pontos de interrupção, consulte [Pausar um código com pontos de interrupção][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="40bbc-194">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="40bbc-195">dir</span><span class="sxs-lookup"><span data-stu-id="40bbc-195">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="40bbc-196">Exibe uma listagem de estilo de objeto de todas as propriedades do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-196">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="40bbc-197">Esse método é um alias para o método [console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="40bbc-197">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="40bbc-198">Avaliar `document.head` no console para exibir o HTML entre as `<head>` marcas e `</head>` .</span><span class="sxs-lookup"><span data-stu-id="40bbc-198">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="40bbc-199">Na [Figura 14](#figure-14), uma listagem de estilo de objeto é exibida após `console.dir()` o uso no console.</span><span class="sxs-lookup"><span data-stu-id="40bbc-199">In [Figure 14](#figure-14), an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

> ##### <span data-ttu-id="40bbc-200">Figura 14</span><span class="sxs-lookup"><span data-stu-id="40bbc-200">Figure 14</span></span>  
> <span data-ttu-id="40bbc-201">Registro `document.head` em log com o `dir()` método</span><span class="sxs-lookup"><span data-stu-id="40bbc-201">Logging `document.head` with `dir()` method</span></span>  
> ![Registrando em log o documento. Head com o método dir ()][ImageLogObject]  

<span data-ttu-id="40bbc-203">Para obter mais informações, consulte a [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrada na API do console.</span><span class="sxs-lookup"><span data-stu-id="40bbc-203">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="40bbc-204">dirxml</span><span class="sxs-lookup"><span data-stu-id="40bbc-204">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="40bbc-205">Imprime uma representação XML do objeto especificado, como visto na guia **elementos** .  Esse método é equivalente ao método [console. DirXML ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="40bbc-205">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="40bbc-206">inspeção</span><span class="sxs-lookup"><span data-stu-id="40bbc-206">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="40bbc-207">Abre e seleciona o elemento ou o objeto especificado no painel apropriado: o painel **elementos** para elementos DOM ou o painel **memória** para objetos de heap JavaScript.</span><span class="sxs-lookup"><span data-stu-id="40bbc-207">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="40bbc-208">Na [Figura 15](#figure-15), o `document.body` abre no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-208">In [Figure 15](#figure-15), the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

> ##### <span data-ttu-id="40bbc-209">Figura 15</span><span class="sxs-lookup"><span data-stu-id="40bbc-209">Figure 15</span></span>  
> <span data-ttu-id="40bbc-210">Inspecionar um elemento com</span><span class="sxs-lookup"><span data-stu-id="40bbc-210">Inspecting an element with</span></span> `inspect()`  
> ![Inspecionar um elemento com inspeção ()][ImageInspectElement]  

<span data-ttu-id="40bbc-212">Ao passar um método para inspecionar, o método abre o documento no painel **fontes** para inspeção.</span><span class="sxs-lookup"><span data-stu-id="40bbc-212">When passing a method to inspect, the method opens the document up in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="40bbc-213">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="40bbc-213">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="40bbc-214">Retorna os ouvintes de eventos registrados no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-214">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="40bbc-215">O valor de retorno é um objeto que contém uma matriz para cada tipo de evento registrado \ (como `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="40bbc-215">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="40bbc-216">Os membros de cada matriz são objetos que descrevem o ouvinte registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="40bbc-216">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="40bbc-217">Na [Figura 16](#figure-16), todos os ouvintes de eventos registrados no objeto do documento são listados.</span><span class="sxs-lookup"><span data-stu-id="40bbc-217">In [Figure 16](#figure-16), all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

> ##### <span data-ttu-id="40bbc-218">Figura 16</span><span class="sxs-lookup"><span data-stu-id="40bbc-218">Figure 16</span></span>  
> <span data-ttu-id="40bbc-219">Saída de uso</span><span class="sxs-lookup"><span data-stu-id="40bbc-219">Output of using</span></span> `getEventListeners(document)`  
> ![Saída do uso de getEventListeners (documento)][ImageGetListeners]  

<span data-ttu-id="40bbc-221">Se mais de um ouvinte estiver registrado no objeto especificado, a matriz contém um membro para cada ouvinte.</span><span class="sxs-lookup"><span data-stu-id="40bbc-221">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="40bbc-222">Na [Figura 16](#figure-16), há dois ouvintes de eventos registrados no elemento do documento para o `click` evento.</span><span class="sxs-lookup"><span data-stu-id="40bbc-222">In [Figure 16](#figure-16), there are two event listeners registered on the document element for the `click` event.</span></span>  

> ##### <span data-ttu-id="40bbc-223">Figura 17</span><span class="sxs-lookup"><span data-stu-id="40bbc-223">Figure 17</span></span>  
> <span data-ttu-id="40bbc-224">Vários ouvintes</span><span class="sxs-lookup"><span data-stu-id="40bbc-224">Multiple listeners</span></span>  
> ![Vários ouvintes][ImageMultipleListeners]  

<span data-ttu-id="40bbc-226">Você pode expandir ainda mais cada um dos seguintes objetos para explorar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="40bbc-226">You may further expand each of the following objects to explore the properties.</span></span>  

> ##### <span data-ttu-id="40bbc-227">Figura 18</span><span class="sxs-lookup"><span data-stu-id="40bbc-227">Figure 18</span></span>  
> <span data-ttu-id="40bbc-228">Exibição expandida do objeto Listener</span><span class="sxs-lookup"><span data-stu-id="40bbc-228">Expanded view of listener object</span></span>  
> ![Exibição expandida do objeto Listener][ImageListenersExpanded]  

## <span data-ttu-id="40bbc-230">chaves</span><span class="sxs-lookup"><span data-stu-id="40bbc-230">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="40bbc-231">Retorna uma matriz que contém os nomes das propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-231">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="40bbc-232">Para obter os valores associados das mesmas propriedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="40bbc-232">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="40bbc-233">Por exemplo, suponha que seu aplicativo definiu o objeto a seguir.</span><span class="sxs-lookup"><span data-stu-id="40bbc-233">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="40bbc-234">Na [Figura 19](#figure-19), o resultado pressupõe `player1` que foi definido no namespace global \ (para simplicidade \) antes de digitar `keys(player1)` e `values(player1)` no console.</span><span class="sxs-lookup"><span data-stu-id="40bbc-234">In [Figure 19](#figure-19), the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### <span data-ttu-id="40bbc-235">Figura 19</span><span class="sxs-lookup"><span data-stu-id="40bbc-235">Figure 19</span></span>  
> <span data-ttu-id="40bbc-236">Os `keys()` `values()` comandos e</span><span class="sxs-lookup"><span data-stu-id="40bbc-236">The `keys()` and `values()` commands</span></span>  
> ![Os comandos Keys () e Values ()][ImageConsoleKeysValues]  

## <span data-ttu-id="40bbc-238">monitor</span><span class="sxs-lookup"><span data-stu-id="40bbc-238">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="40bbc-239">Registra uma mensagem no console que indica o nome do método juntamente com os argumentos que são passados para o método quando ele é chamado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-239">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### <span data-ttu-id="40bbc-240">Figura 20</span><span class="sxs-lookup"><span data-stu-id="40bbc-240">Figure 20</span></span>  
> <span data-ttu-id="40bbc-241">O `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="40bbc-241">The `monitor()` method</span></span>  
> ![O método monitor ()][ImageConsoleMonitorSum]  

<span data-ttu-id="40bbc-243">Use `unmonitor(method)` para interromper o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="40bbc-243">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="40bbc-244">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="40bbc-244">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="40bbc-245">Quando ocorre um dos eventos especificados no objeto especificado, o objeto de evento é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="40bbc-245">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="40bbc-246">Você pode especificar um único evento para monitorar, uma matriz de eventos ou um dos tipos de eventos genéricos que são mapeados para uma coleção predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="40bbc-246">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="40bbc-247">Veja a [Figura 21](#figure-21).</span><span class="sxs-lookup"><span data-stu-id="40bbc-247">See [Figure 21](#figure-21).</span></span>  

<span data-ttu-id="40bbc-248">Os seguintes monitores redimensionam eventos no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="40bbc-248">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

> ##### <span data-ttu-id="40bbc-249">Figura 21</span><span class="sxs-lookup"><span data-stu-id="40bbc-249">Figure 21</span></span>  
> <span data-ttu-id="40bbc-250">Janela de monitoramento redimensionar eventos</span><span class="sxs-lookup"><span data-stu-id="40bbc-250">Monitoring window resize events</span></span>  
> ![Janela de monitoramento redimensionar eventos][ImageMonitorResize]  

<span data-ttu-id="40bbc-252">O seguinte define uma matriz para monitorar os dois `resize` e os `scroll` eventos no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="40bbc-252">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="40bbc-253">Você também pode especificar um dos tipos de eventos disponíveis, cadeias de caracteres que são mapeados para conjuntos de eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="40bbc-253">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="40bbc-254">A tabela a seguir mostra os tipos de eventos disponíveis e os mapeamentos de eventos associados.</span><span class="sxs-lookup"><span data-stu-id="40bbc-254">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="40bbc-255">Event type</span><span class="sxs-lookup"><span data-stu-id="40bbc-255">Event type</span></span> | <span data-ttu-id="40bbc-256">Eventos mapeados correspondentes</span><span class="sxs-lookup"><span data-stu-id="40bbc-256">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="40bbc-257">"clique em", "DblClick", "botão de mouse", "MouseUp", "mouseout", "mouse pressionado", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="40bbc-257">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="40bbc-258">"KeyDown", "KeyPress", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="40bbc-258">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="40bbc-259">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="40bbc-259">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="40bbc-260">"Blur", "alterar", "enfocar", "selecionar", "enviar", "zoom", "selecionar", "enviar", "zoom"</span><span class="sxs-lookup"><span data-stu-id="40bbc-260">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="40bbc-261">Na [Figura 22](#figure-22), o `key` tipo de evento correspondente a `key` eventos em um campo de texto de entrada está selecionado atualmente no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-261">In [Figure 22](#figure-22), the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="40bbc-262">Na [Figura 22](#figure-22) a saída do exemplo após a digitação de um caractere no campo de texto é exibida.</span><span class="sxs-lookup"><span data-stu-id="40bbc-262">In [Figure 22](#figure-22) the sample output after typing a character in the text field is displayed.</span></span>  

> ##### <span data-ttu-id="40bbc-263">Figura 22</span><span class="sxs-lookup"><span data-stu-id="40bbc-263">Figure 22</span></span>  
> <span data-ttu-id="40bbc-264">Monitorar eventos chave</span><span class="sxs-lookup"><span data-stu-id="40bbc-264">Monitoring key events</span></span>  
> ![Monitorar eventos chave][ImageMonitorKey]  

## <span data-ttu-id="40bbc-266">profile</span><span class="sxs-lookup"><span data-stu-id="40bbc-266">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="40bbc-267">Inicia uma sessão de criação de perfil de CPU JavaScript com um nome opcional.</span><span class="sxs-lookup"><span data-stu-id="40bbc-267">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="40bbc-268">O método [profileEnd ()](#profileend) conclui o perfil e exibe os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-268">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="40bbc-269">Execute o `profile()` método para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="40bbc-269">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="40bbc-270">Execute o método [profileEnd ()](#profileend) para interromper a criação de perfil e exibir os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-270">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="40bbc-271">Perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="40bbc-271">Profiles may also be nested.</span></span>  <span data-ttu-id="40bbc-272">Na [Figura 23](#figure-23) , o resultado é o mesmo, independentemente da ordem.</span><span class="sxs-lookup"><span data-stu-id="40bbc-272">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="40bbc-273">Vários perfis de CPU podem operar ao mesmo tempo e não é necessário fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="40bbc-273">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="40bbc-274">profileEnd</span><span class="sxs-lookup"><span data-stu-id="40bbc-274">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="40bbc-275">Conclui uma sessão de criação de perfil de CPU JavaScript e exibe os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-275">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="40bbc-276">Você deve estar executando o método [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="40bbc-276">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="40bbc-277">Execute o método [Profile ()](#profile) para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="40bbc-277">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="40bbc-278">Execute o `profileEnd()` método para interromper a criação de perfil e exibir os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-278">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="40bbc-279">Perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="40bbc-279">Profiles may also be nested.</span></span>  <span data-ttu-id="40bbc-280">Na [Figura 23](#figure-23) , o resultado é o mesmo, independentemente da ordem.</span><span class="sxs-lookup"><span data-stu-id="40bbc-280">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="40bbc-281">O resultado aparece como um instantâneo de heap no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="40bbc-281">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="40bbc-282">Figura 23</span><span class="sxs-lookup"><span data-stu-id="40bbc-282">Figure 23</span></span>  
> <span data-ttu-id="40bbc-283">Perfis agrupados</span><span class="sxs-lookup"><span data-stu-id="40bbc-283">Grouped profiles</span></span>  
> ![Perfis agrupados][ImageGroupedProfiles]  

> [!NOTE]
> <span data-ttu-id="40bbc-285">Vários perfis de CPU podem operar ao mesmo tempo e não é necessário fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="40bbc-285">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="40bbc-286">TableName</span><span class="sxs-lookup"><span data-stu-id="40bbc-286">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="40bbc-287">Registra dados de objeto com formatação de tabela com base no objeto de dados em títulos de coluna opcionais.</span><span class="sxs-lookup"><span data-stu-id="40bbc-287">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="40bbc-288">Na [Figura 24](#figure-24), é exibida uma lista de nomes usando uma tabela no console.</span><span class="sxs-lookup"><span data-stu-id="40bbc-288">In [Figure 24](#figure-24), a list of names using a table in the console is displayed.</span></span>  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

> ##### <span data-ttu-id="40bbc-289">Figura 24</span><span class="sxs-lookup"><span data-stu-id="40bbc-289">Figure 24</span></span>  
> <span data-ttu-id="40bbc-290">O `table()` método</span><span class="sxs-lookup"><span data-stu-id="40bbc-290">The `table()` method</span></span>  
> ![O método Table ()][ImageConsoleTable]  

## <span data-ttu-id="40bbc-292">desdepurar</span><span class="sxs-lookup"><span data-stu-id="40bbc-292">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="40bbc-293">Interrompe a depuração do método especificado para que, quando o método for chamado, o depurador não seja mais invocado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-293">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="40bbc-294">desmonitorar</span><span class="sxs-lookup"><span data-stu-id="40bbc-294">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="40bbc-295">Interrompe o monitoramento do método especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-295">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="40bbc-296">Isso é usado em conjunto com o método [Monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="40bbc-296">This is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="40bbc-297">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="40bbc-297">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="40bbc-298">Interrompe o monitoramento de eventos do objeto e dos eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="40bbc-298">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="40bbc-299">Por exemplo, o seguinte interrompe todos os monitoramentos de evento no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="40bbc-299">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="40bbc-300">Você também pode parar seletivamente o monitoramento de eventos específicos em um objeto.</span><span class="sxs-lookup"><span data-stu-id="40bbc-300">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="40bbc-301">Por exemplo, o código a seguir começa a monitorar todos os `mouse` eventos no elemento atualmente selecionado e, em seguida, interrompe o monitoramento de `mousemove` eventos \ (talvez reduzir o ruído na saída do console \).</span><span class="sxs-lookup"><span data-stu-id="40bbc-301">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="40bbc-302">valores</span><span class="sxs-lookup"><span data-stu-id="40bbc-302">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="40bbc-303">Retorna uma matriz que contém os valores de todas as propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbc-303">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Figura 1: $ _ é a expressão avaliada mais recentemente"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Figura 2: $ _ muda quando novos comandos são avaliados"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Figura 3: o $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Figura 4: o $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Figura 5: o $ (' img ')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Figura 6: $ (' img '). src"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Figura 7: $ (' img ', Document. querySelector (' título--imagem ')). src"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Figura 8: usando $ $ () para selecionar todas as imagens no documento e exibir as fontes"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Figura 9: usando $ $ () para selecionar todas as imagens que aparecem após o <div especificado> o elemento no documento e exibir as fontes"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Figura 10: usando um seletor XPath"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Figura 11: usando um seletor XPath mais complicado"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Figura 12: usando um seletor XPath com startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Figura 13: quebrando dentro de um método com o depurador ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Figura 14: registrando o documento. Body com o método dir ()"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Figura 15: inspecionar um elemento com inspecionar ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Figura 16: saída do uso de getEventListeners (documento)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Figura 17: vários ouvintes"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Figura 18: exibição expandida do objeto Listener"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Figura 19: os comandos Keys () e Values ()"  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Figura 20: o método monitor ()"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Figura 21: monitorar eventos do Window Resize"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Figura 22: monitorar eventos de chave"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Figura 23: perfis agrupados"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Figura 24: o método Table ()"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Dir-referência de API do console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Como pausar um código com pontos de interrupção no Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar o tempo de execução do JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: a depuração (função) não está funcionando | Monorail"  

> [!NOTE]
> <span data-ttu-id="40bbc-337">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="40bbc-337">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="40bbc-338">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/utilities) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="40bbc-338">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="40bbc-340">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="40bbc-340">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
