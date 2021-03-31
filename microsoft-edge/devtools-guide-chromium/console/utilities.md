---
description: Uma referência de comandos de conveniência disponíveis no Console do Microsoft Edge DevTools.
title: Referência da API de Utilitários de Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398823"
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

# <a name="console-utilities-api-reference"></a><span data-ttu-id="9b133-104">Referência da API de Utilitários de Console</span><span class="sxs-lookup"><span data-stu-id="9b133-104">Console Utilities API reference</span></span>  

<span data-ttu-id="9b133-105">A API de Utilitários de Console contém uma coleção de comandos de conveniência para executar tarefas comuns: selecionar e inspecionar elementos DOM, exibir dados em formato acessível, interromper e iniciar o profiler e monitorar eventos DOM.</span><span class="sxs-lookup"><span data-stu-id="9b133-105">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="9b133-106">Os comandos a seguir só funcionam no Console do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9b133-106">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="9b133-107">Os comandos não funcionarão se executados de seus scripts.</span><span class="sxs-lookup"><span data-stu-id="9b133-107">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="9b133-108">Para os `console.log()` métodos e o restante dos `console.error()` `console.*` métodos, navegue até [Console API Reference][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="9b133-108">For the `console.log()` and `console.error()` methods the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="9b133-109">Expressão avaliada recentemente</span><span class="sxs-lookup"><span data-stu-id="9b133-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="9b133-110">Retorna o valor da expressão avaliada mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="9b133-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="9b133-111">Na figura a seguir, uma expressão simples \( `2 + 2` \) é avaliada.</span><span class="sxs-lookup"><span data-stu-id="9b133-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="9b133-112">Em `$_` seguida, a propriedade é avaliada, que contém o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="9b133-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ é a expressão avaliada mais recentemente" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="9b133-114">Figura 1:  `$_` é a expressão avaliada mais recentemente</span><span class="sxs-lookup"><span data-stu-id="9b133-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-115">Na figura a seguir, a expressão avaliada inicialmente contém uma matriz de nomes.</span><span class="sxs-lookup"><span data-stu-id="9b133-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="9b133-116">Avaliando para encontrar o comprimento da matriz, o valor armazenado em alterações para se tornar a expressão avaliada mais `$_.length` `$_` recente, `4` .</span><span class="sxs-lookup"><span data-stu-id="9b133-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ muda quando novos comandos são avaliados" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="9b133-118">Figura 2:  `$_` alterações quando novos comandos são avaliados</span><span class="sxs-lookup"><span data-stu-id="9b133-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="9b133-119">Elemento escolhido recentemente ou objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="9b133-119">Recently Chosen Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="9b133-120">Retorna o elemento selecionado mais recentemente ou o objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9b133-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="9b133-121">retorna o segundo selecionado mais recentemente e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9b133-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="9b133-122">Os comandos , , e funcionam como uma referência histórica aos últimos cinco elementos DOM inspecionados na ferramenta Elements ou os cinco últimos objetos de pilha JavaScript selecionados na `$0` `$1` ferramenta `$2` `$3` `$4` **Memória.** </span><span class="sxs-lookup"><span data-stu-id="9b133-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects selected in the **Memory** tool.</span></span>  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

<span data-ttu-id="9b133-123">Na figura a seguir, um `img` elemento é selecionado na ferramenta **Elements.**</span><span class="sxs-lookup"><span data-stu-id="9b133-123">In the following figure, an `img` element is selected in the **Elements** tool.</span></span>  <span data-ttu-id="9b133-124">Na gaveta **Console,** `$0` foi avaliado e exibe o mesmo elemento.</span><span class="sxs-lookup"><span data-stu-id="9b133-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Os $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="9b133-126">Figura 3: O</span><span class="sxs-lookup"><span data-stu-id="9b133-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="9b133-127">Na figura a seguir, a imagem mostra um elemento diferente selecionado na mesma página.</span><span class="sxs-lookup"><span data-stu-id="9b133-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="9b133-128">O `$0` agora se refere ao elemento recém-selecionado, enquanto retorna o elemento selecionado `$1` anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9b133-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="O $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="9b133-130">Figura 4: O</span><span class="sxs-lookup"><span data-stu-id="9b133-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <a name="query-selector"></a><span data-ttu-id="9b133-131">Seletor de consulta</span><span class="sxs-lookup"><span data-stu-id="9b133-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="9b133-132">Retorna a referência ao primeiro elemento DOM com o seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="9b133-133">Este método é um alias para o [método document.querySelector().][MDNDocumentQuerySelector]</span><span class="sxs-lookup"><span data-stu-id="9b133-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="9b133-134">Na figura a seguir, uma referência ao primeiro `<img>` elemento do documento é retornada.</span><span class="sxs-lookup"><span data-stu-id="9b133-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="9b133-136">Figura 5: O</span><span class="sxs-lookup"><span data-stu-id="9b133-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="9b133-137">Passe o mouse no resultado retornado, abra o menu contextual \(clique com o botão  direito do mouse\) e escolha **Revelar** no Painel de Elementos para encontrá-lo no DOM ou Role para Exibir para exibi-lo na página.</span><span class="sxs-lookup"><span data-stu-id="9b133-137">Hover on the returned result, open the contextual menu \(right-click\), and choose **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="9b133-138">Na figura a seguir, uma referência ao elemento selecionado no momento é retornada e a propriedade src é exibida.</span><span class="sxs-lookup"><span data-stu-id="9b133-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="9b133-140">Figura 6: O</span><span class="sxs-lookup"><span data-stu-id="9b133-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="9b133-141">Esse método também dá suporte a um segundo parâmetro, startNode, que especifica um "elemento" ou Nó do qual procurar elementos.</span><span class="sxs-lookup"><span data-stu-id="9b133-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="9b133-142">O valor padrão do parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="9b133-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="9b133-143">Na figura a seguir, o primeiro `img` elemento é encontrado depois que o e exibe `title--image` `src` corretamente é retornado.</span><span class="sxs-lookup"><span data-stu-id="9b133-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="9b133-145">Figura 7: O</span><span class="sxs-lookup"><span data-stu-id="9b133-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9b133-146">Se você estiver usando uma biblioteca como jQuery que usa , a funcionalidade será substituída e corresponderá à implementação `$` `$` dessa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9b133-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <a name="query-selector-all"></a><span data-ttu-id="9b133-147">Seletor de Consulta Todos</span><span class="sxs-lookup"><span data-stu-id="9b133-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="9b133-148">Retorna uma matriz de elementos que corresponderão ao seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="9b133-149">Esse método equivale a executar o [método document.querySelectorAll().][MDNDocumentQuerySelectorAll]</span><span class="sxs-lookup"><span data-stu-id="9b133-149">This method is equivalent to running the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="9b133-150">Na figura e exemplo de código a seguir, use para criar uma matriz de todos os elementos no documento atual e exibir o valor da propriedade `$$()` `<img>` para cada `src` elemento.</span><span class="sxs-lookup"><span data-stu-id="9b133-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Usando $$() para selecionar todas as imagens no documento e exibir as fontes" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="9b133-152">Figura 8: Usando `$$()` para selecionar todas as imagens no documento e exibir as fontes</span><span class="sxs-lookup"><span data-stu-id="9b133-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-153">Este método também dá suporte a um segundo parâmetro, startNode, que especifica um elemento ou Nó do qual procurar elementos.</span><span class="sxs-lookup"><span data-stu-id="9b133-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="9b133-154">O valor padrão do parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="9b133-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="9b133-155">Na figura e amostra de código a seguir, uma versão modificada do exemplo de código anterior e a figura usam para criar uma matriz de todos os elementos que aparecem no documento atual após o `$$()` `<img>` Nó selecionado.</span><span class="sxs-lookup"><span data-stu-id="9b133-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usando $$() para selecionar todas as imagens que aparecem após o elemento <div> no documento e exibir as fontes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="9b133-157">Figura 9: Usando para selecionar todas as imagens que aparecem após `$$()` o elemento especificado no documento e exibir as `<div>` fontes</span><span class="sxs-lookup"><span data-stu-id="9b133-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9b133-158">Selecione `Shift` + `Enter` no console para iniciar uma nova linha sem executar o script.</span><span class="sxs-lookup"><span data-stu-id="9b133-158">Select `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <a name="xpath"></a><span data-ttu-id="9b133-159">XPath</span><span class="sxs-lookup"><span data-stu-id="9b133-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="9b133-160">Retorna uma matriz de elementos DOM que corresponderão à expressão XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="9b133-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="9b133-161">Na figura e amostra de código a seguir, todos os `<p>` elementos na página são retornados.</span><span class="sxs-lookup"><span data-stu-id="9b133-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Usando um seletor XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="9b133-163">Figura 10: Usando um seletor XPath</span><span class="sxs-lookup"><span data-stu-id="9b133-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-164">Na figura e amostra de código a seguir, todos os `<p>` elementos que contêm `<a>` elementos são retornados.</span><span class="sxs-lookup"><span data-stu-id="9b133-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Usando um seletor XPath mais complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="9b133-166">Figura 11: Usando um seletor XPath mais complicado</span><span class="sxs-lookup"><span data-stu-id="9b133-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-167">Semelhante aos outros comandos do seletor, tem um segundo parâmetro opcional, , que especifica um elemento ou Nó do qual `$x(path)` `startNode` procurar elementos.</span><span class="sxs-lookup"><span data-stu-id="9b133-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Usando um seletor XPath com startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="9b133-169">Figura 12: Usando um seletor XPath com</span><span class="sxs-lookup"><span data-stu-id="9b133-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <a name="clear"></a><span data-ttu-id="9b133-170">clear</span><span class="sxs-lookup"><span data-stu-id="9b133-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="9b133-171">Limpa o console do histórico.</span><span class="sxs-lookup"><span data-stu-id="9b133-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="9b133-172">copy</span><span class="sxs-lookup"><span data-stu-id="9b133-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="9b133-173">O `copy(object)` método copia uma representação de cadeia de caracteres do objeto especificado para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="9b133-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <a name="debug"></a><span data-ttu-id="9b133-174">depurar</span><span class="sxs-lookup"><span data-stu-id="9b133-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="9b133-175">O [problema do Chromium #1050237][MonorailIssue1050237] está rastreando um bug com a `debug()` função.</span><span class="sxs-lookup"><span data-stu-id="9b133-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="9b133-176">Se você encontrar o problema, tente [usar pontos de interrupção.][DevtoolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="9b133-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="9b133-177">Quando você solicita o método especificado, o depurador é invocado e quebra dentro do método na ferramenta **Sources,** permitindo passar pelo código e depurá-lo.</span><span class="sxs-lookup"><span data-stu-id="9b133-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** tool allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Quebrar dentro de um método com depuração()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="9b133-179">Figura 13: Quebrar dentro de um método com</span><span class="sxs-lookup"><span data-stu-id="9b133-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="9b133-180">Use para parar de quebrar o método ou use a interface do usuário `undebug(method)` para desabilitar todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="9b133-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="9b133-181">Para obter mais informações sobre pontos de interrupção, navegue até [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="9b133-181">For more information on breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="dir"></a><span data-ttu-id="9b133-182">dir</span><span class="sxs-lookup"><span data-stu-id="9b133-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="9b133-183">Exibe uma listagem de estilo de objeto de todas as propriedades do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="9b133-184">Este método é um alias para o [método console.dir().][MDNConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="9b133-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="9b133-185">Avalie `document.head` no Console para exibir o HTML entre as marcas `<head>` `</head>` e.</span><span class="sxs-lookup"><span data-stu-id="9b133-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="9b133-186">Na figura e exemplo de código a seguir, uma listagem de estilo de objeto é exibida após o `console.dir()` uso no Console.</span><span class="sxs-lookup"><span data-stu-id="9b133-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Método log document.head com dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="9b133-188">Figura 14: Log `document.head` com `dir()` método</span><span class="sxs-lookup"><span data-stu-id="9b133-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-189">Para obter mais informações, navegue [`console.dir()`][DevToolsConsoleApiConsoleDirObject] até a entrada na API do Console.</span><span class="sxs-lookup"><span data-stu-id="9b133-189">For more information, navigate to [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <a name="dirxml"></a><span data-ttu-id="9b133-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="9b133-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="9b133-191">Imprime uma representação XML do objeto especificado, conforme exibido na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="9b133-191">Prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="9b133-192">Esse método é equivalente ao [método console.dirxml().][MDNConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="9b133-192">This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <a name="inspect"></a><span data-ttu-id="9b133-193">inspect</span><span class="sxs-lookup"><span data-stu-id="9b133-193">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="9b133-194">Abre e seleciona o elemento ou objeto especificado no painel apropriado: a ferramenta **Elements** para elementos DOM ou a ferramenta **Memória** para objetos de pilha JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9b133-194">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

<span data-ttu-id="9b133-195">Na figura e amostra de código a seguir, a `document.body` abre na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="9b133-195">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspecionar um elemento com inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="9b133-197">Figura 15: Inspecionar um elemento com</span><span class="sxs-lookup"><span data-stu-id="9b133-197">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="9b133-198">Ao passar um método para inspecionar, o método abre o documento na **ferramenta Fontes** para você inspecionar.</span><span class="sxs-lookup"><span data-stu-id="9b133-198">When passing a method to inspect, the method opens the document in the **Sources** tool for you to inspect.</span></span>  

## <a name="geteventlisteners"></a><span data-ttu-id="9b133-199">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="9b133-199">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="9b133-200">Retorna os ouvintes de eventos registrados no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-200">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="9b133-201">O valor de retorno é um objeto que contém uma matriz para cada tipo de evento registrado \(como `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="9b133-201">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="9b133-202">Os membros de cada matriz são objetos que descrevem o ouvinte registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="9b133-202">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="9b133-203">Na figura de exemplo de código a seguir, todos os ouvintes de eventos registrados no objeto do documento são listados.</span><span class="sxs-lookup"><span data-stu-id="9b133-203">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Saída do uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="9b133-205">Figura 16: O resultado do uso</span><span class="sxs-lookup"><span data-stu-id="9b133-205">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="9b133-206">Se mais de um ouvinte estiver registrado no objeto especificado, a matriz conterá um membro para cada ouvinte.</span><span class="sxs-lookup"><span data-stu-id="9b133-206">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="9b133-207">Na figura a seguir, há dois ouvintes de eventos registrados no elemento de documento do `click` evento.</span><span class="sxs-lookup"><span data-stu-id="9b133-207">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Vários ouvintes" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="9b133-209">Figura 17: Vários ouvintes</span><span class="sxs-lookup"><span data-stu-id="9b133-209">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-210">Você pode expandir ainda mais cada um dos objetos a seguir para explorar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="9b133-210">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Exibição expandida do objeto ouvinte" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="9b133-212">Figura 18: Exibição expandida do objeto ouvinte</span><span class="sxs-lookup"><span data-stu-id="9b133-212">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <a name="keys"></a><span data-ttu-id="9b133-213">chaves</span><span class="sxs-lookup"><span data-stu-id="9b133-213">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="9b133-214">Retorna uma matriz que contém os nomes das propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-214">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="9b133-215">Para obter os valores associados das mesmas propriedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="9b133-215">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="9b133-216">Por exemplo, suponha que seu aplicativo definiu o objeto a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b133-216">For example, suppose your application defined the following object.</span></span>  

```console
var player1 =   
```  

<span data-ttu-id="9b133-217">Na figura e amostras de código a seguir, o resultado supõe que foi definido no `player1` namespace global \(for simplicity\) antes de digitar e `keys(player1)` no `values(player1)` console.</span><span class="sxs-lookup"><span data-stu-id="9b133-217">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Os comandos keys() e values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="9b133-219">Figura 19: Os `keys()` comandos e `values()`</span><span class="sxs-lookup"><span data-stu-id="9b133-219">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <a name="monitor"></a><span data-ttu-id="9b133-220">monitor</span><span class="sxs-lookup"><span data-stu-id="9b133-220">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="9b133-221">Registra uma mensagem no console que indica o nome do método juntamente com os argumentos que são passados para o método quando ele foi chamado.</span><span class="sxs-lookup"><span data-stu-id="9b133-221">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="O método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="9b133-223">Figura 20: O `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="9b133-223">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-224">Use `unmonitor(method)` para interromper o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="9b133-224">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <a name="monitorevents"></a><span data-ttu-id="9b133-225">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="9b133-225">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="9b133-226">Quando um dos eventos especificados ocorre no objeto especificado, o objeto de evento é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="9b133-226">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="9b133-227">Você pode especificar um único evento a ser monitorado, uma matriz de eventos ou um dos tipos de eventos genéricos mapeados para uma coleção predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="9b133-227">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="9b133-228">Revise o exemplo de código a seguir e a figura.</span><span class="sxs-lookup"><span data-stu-id="9b133-228">Review the following code sample and figure.</span></span>  

<span data-ttu-id="9b133-229">O seguinte monitora todos os eventos de resize no objeto window.</span><span class="sxs-lookup"><span data-stu-id="9b133-229">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Monitoring window resize events" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="9b133-231">Figura 21: Monitoring window resize events</span><span class="sxs-lookup"><span data-stu-id="9b133-231">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="9b133-232">O seguinte define uma matriz para monitorar eventos `resize` e ambos no objeto `scroll` window.</span><span class="sxs-lookup"><span data-stu-id="9b133-232">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="9b133-233">Você também pode especificar um dos tipos de eventos disponíveis, cadeias de caracteres que mapeiam para conjuntos predefinidos de eventos.</span><span class="sxs-lookup"><span data-stu-id="9b133-233">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="9b133-234">A tabela a seguir exibe os tipos de eventos disponíveis e os mapeamentos de eventos associados.</span><span class="sxs-lookup"><span data-stu-id="9b133-234">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="9b133-235">Event type</span><span class="sxs-lookup"><span data-stu-id="9b133-235">Event type</span></span> | <span data-ttu-id="9b133-236">Eventos mapeados correspondentes</span><span class="sxs-lookup"><span data-stu-id="9b133-236">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="9b133-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span><span class="sxs-lookup"><span data-stu-id="9b133-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="9b133-238">"keydown", "keypress", "keyup", "textInput"</span><span class="sxs-lookup"><span data-stu-id="9b133-238">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="9b133-239">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="9b133-239">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="9b133-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span><span class="sxs-lookup"><span data-stu-id="9b133-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="9b133-241">No exemplo de código a seguir, o tipo de evento correspondente a eventos em um campo de texto de entrada está atualmente `key` `key` selecionado na ferramenta **Elements.**</span><span class="sxs-lookup"><span data-stu-id="9b133-241">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="9b133-242">Na figura a seguir, a saída de exemplo após digitar um caractere no campo de texto é exibida.</span><span class="sxs-lookup"><span data-stu-id="9b133-242">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Monitorando os principais eventos" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="9b133-244">Figura 22: Monitorando os principais eventos</span><span class="sxs-lookup"><span data-stu-id="9b133-244">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <a name="profile"></a><span data-ttu-id="9b133-245">profile</span><span class="sxs-lookup"><span data-stu-id="9b133-245">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="9b133-246">Inicia uma sessão de criação de perfil de CPU JavaScript com um nome opcional.</span><span class="sxs-lookup"><span data-stu-id="9b133-246">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="9b133-247">O [método profileEnd()](#profileend) conclui o perfil e exibe os resultados na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="9b133-247">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="9b133-248">Execute o `profile()` método para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="9b133-248">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="9b133-249">Execute o [método profileEnd()](#profileend) para interromper a criação de perfil e exibir os resultados na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="9b133-249">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="9b133-250">Os perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="9b133-250">Profiles may also be nested.</span></span>  <span data-ttu-id="9b133-251">Nos exemplos de código a seguir e figurar o resultado é o mesmo, independentemente da ordem.</span><span class="sxs-lookup"><span data-stu-id="9b133-251">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="9b133-252">Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="9b133-252">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="profileend"></a><span data-ttu-id="9b133-253">profileEnd</span><span class="sxs-lookup"><span data-stu-id="9b133-253">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="9b133-254">Conclui uma sessão de criação de perfil de CPU JavaScript e exibe os resultados na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="9b133-254">Completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="9b133-255">Você deve estar executando o [método profile().](#profile)</span><span class="sxs-lookup"><span data-stu-id="9b133-255">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="9b133-256">Execute o [método profile()](#profile) para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="9b133-256">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="9b133-257">Execute o `profileEnd()` método para interromper a criação de perfil e exibir os resultados na ferramenta **Memória.**</span><span class="sxs-lookup"><span data-stu-id="9b133-257">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="9b133-258">Os perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="9b133-258">Profiles may also be nested.</span></span>  <span data-ttu-id="9b133-259">No exemplo de código a seguir e figura o resultado é o mesmo, independentemente da ordem.</span><span class="sxs-lookup"><span data-stu-id="9b133-259">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="9b133-260">O resultado aparece como um Instantâneo de Pilha na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="9b133-260">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfis agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="9b133-262">Figura 23: Perfis agrupados</span><span class="sxs-lookup"><span data-stu-id="9b133-262">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9b133-263">Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="9b133-263">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="queryobjects"></a><span data-ttu-id="9b133-264">queryObjects</span><span class="sxs-lookup"><span data-stu-id="9b133-264">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="9b133-265">Retornar uma matriz de objetos criados com o construtor especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-265">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="9b133-266">O escopo de é o contexto de tempo de execução `queryObjects()` selecionado no console.</span><span class="sxs-lookup"><span data-stu-id="9b133-266">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="9b133-267">Retorna todos `Promises` .</span><span class="sxs-lookup"><span data-stu-id="9b133-267">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="9b133-268">Retorna todos os elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="9b133-268">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="9b133-269">Retorna todos os objetos que foram instautados usando `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="9b133-269">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="9b133-270">table</span><span class="sxs-lookup"><span data-stu-id="9b133-270">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="9b133-271">Registra dados de objeto com formatação de tabela com base no objeto de dados em com títulos opcionais de coluna.</span><span class="sxs-lookup"><span data-stu-id="9b133-271">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="9b133-272">Na figura e exemplo de código a seguir, uma lista de nomes usando uma tabela no console é exibida.</span><span class="sxs-lookup"><span data-stu-id="9b133-272">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="O resultado do método table()" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="9b133-274">Figura 24: O resultado do `table()` método</span><span class="sxs-lookup"><span data-stu-id="9b133-274">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <a name="undebug"></a><span data-ttu-id="9b133-275">undebug</span><span class="sxs-lookup"><span data-stu-id="9b133-275">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="9b133-276">Interrompe a depuração do método especificado para que, quando o método for chamado, o depurador não seja mais invocado.</span><span class="sxs-lookup"><span data-stu-id="9b133-276">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <a name="unmonitor"></a><span data-ttu-id="9b133-277">unmonitor</span><span class="sxs-lookup"><span data-stu-id="9b133-277">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="9b133-278">Interrompe o monitoramento do método especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-278">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="9b133-279">Esse método é usado em conjunto com o [método monitor().](#monitor)</span><span class="sxs-lookup"><span data-stu-id="9b133-279">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a><span data-ttu-id="9b133-280">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="9b133-280">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="9b133-281">Interrompe o monitoramento de eventos para o objeto e eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="9b133-281">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="9b133-282">Por exemplo, o seguinte interrompe todo o monitoramento de eventos no objeto window.</span><span class="sxs-lookup"><span data-stu-id="9b133-282">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="9b133-283">Você também pode parar seletivamente o monitoramento de eventos específicos em um objeto.</span><span class="sxs-lookup"><span data-stu-id="9b133-283">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="9b133-284">Por exemplo, o código a seguir começa a monitorar todos os eventos no elemento selecionado no momento e interrompe o monitoramento de eventos \(talvez para reduzir o ruído na saída `mouse` `mousemove` do console\).</span><span class="sxs-lookup"><span data-stu-id="9b133-284">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a><span data-ttu-id="9b133-285">values</span><span class="sxs-lookup"><span data-stu-id="9b133-285">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="9b133-286">Retorna uma matriz que contém os valores de todas as propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b133-286">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9b133-287">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9b133-287">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência da API do Console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir - Referência da API de Console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar o tempo de execução do JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: depuração(função) não está funcionando | Monotrilho"  

> [!NOTE]
> <span data-ttu-id="9b133-297">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b133-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9b133-298">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/utilities) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9b133-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9b133-300">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b133-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
