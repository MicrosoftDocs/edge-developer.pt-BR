---
title: Referência de API de utilitários de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: efa03e02813d718514f73445bc0dceb3a1a83f39
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708753"
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

# <span data-ttu-id="6a584-103">Referência de API de utilitários de console</span><span class="sxs-lookup"><span data-stu-id="6a584-103">Console Utilities API Reference</span></span>  

<span data-ttu-id="6a584-104">A API de utilitários de console contém um conjunto de comandos de conveniência para realizar tarefas comuns: selecionando e inspecionando os elementos DOM, exibindo dados em um formato legível, interrompendo e iniciando o gerador de perfil e monitorando eventos DOM.</span><span class="sxs-lookup"><span data-stu-id="6a584-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="6a584-105">Os comandos a seguir só funcionam no console Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="6a584-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="6a584-106">Os comandos não funcionam se forem executados a partir de seus scripts.</span><span class="sxs-lookup"><span data-stu-id="6a584-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="6a584-107">Procurando `console.log()` , `console.error()` e o restante dos `console.*` métodos?</span><span class="sxs-lookup"><span data-stu-id="6a584-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="6a584-108">Consulte [referência de API do console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="6a584-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="6a584-109">Expressão avaliada recentemente</span><span class="sxs-lookup"><span data-stu-id="6a584-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="6a584-110">Retorna o valor da expressão avaliada mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="6a584-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="6a584-111">Na figura a seguir, uma expressão simples \ ( `2 + 2` \) é avaliada.</span><span class="sxs-lookup"><span data-stu-id="6a584-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="6a584-112">A `$_` propriedade é então avaliada, que contém o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="6a584-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ é a expressão avaliada mais recentemente" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="6a584-114">Figura 1: `$_` a expressão avaliada mais recentemente</span><span class="sxs-lookup"><span data-stu-id="6a584-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-115">Na figura a seguir, a expressão avaliada inicialmente contém uma matriz de nomes.</span><span class="sxs-lookup"><span data-stu-id="6a584-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="6a584-116">Avaliando `$_.length` para localizar o comprimento da matriz, o valor armazenado em `$_` alterações para se tornar a expressão avaliada mais recente `4` .</span><span class="sxs-lookup"><span data-stu-id="6a584-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ muda quando novos comandos são avaliados" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="6a584-118">Figura 2: `$_` alterações quando novos comandos são avaliados</span><span class="sxs-lookup"><span data-stu-id="6a584-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <span data-ttu-id="6a584-119">Elemento ou objeto JavaScript selecionado recentemente</span><span class="sxs-lookup"><span data-stu-id="6a584-119">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="6a584-120">Retorna o elemento do elemento JavaScript ou o objeto selecionado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="6a584-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="6a584-121">Retorna a segunda opção selecionada mais recentemente e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6a584-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="6a584-122">Os `$0` comandos,,, `$1` `$2` `$3` e `$4` funcionam como uma referência histórica aos cinco últimos elementos DOM inspecionados no painel **elementos** ou nos últimos cinco objetos de heap JavaScript selecionados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="6a584-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

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

<span data-ttu-id="6a584-123">Na figura a seguir, um `img` elemento é selecionado no painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="6a584-123">In the following figure, an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="6a584-124">Na gaveta do **console** , foi `$0` avaliada e exibe o mesmo elemento.</span><span class="sxs-lookup"><span data-stu-id="6a584-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="O $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="6a584-126">Figura 3: o</span><span class="sxs-lookup"><span data-stu-id="6a584-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="6a584-127">Na figura a seguir, a imagem mostra um elemento diferente selecionado na mesma página.</span><span class="sxs-lookup"><span data-stu-id="6a584-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="6a584-128">O `$0` agora se refere ao elemento selecionado recentemente, enquanto `$1` retorna o anterior selecionado.</span><span class="sxs-lookup"><span data-stu-id="6a584-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="O $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="6a584-130">Figura 4: o</span><span class="sxs-lookup"><span data-stu-id="6a584-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <span data-ttu-id="6a584-131">Seletor de consulta</span><span class="sxs-lookup"><span data-stu-id="6a584-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="6a584-132">Retorna a referência ao primeiro elemento DOM com o seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="6a584-133">Esse método é um alias para o método [Document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="6a584-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="6a584-134">Na figura a seguir, uma referência para o primeiro `<img>` elemento no documento é retornada.</span><span class="sxs-lookup"><span data-stu-id="6a584-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ (' Img ')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="6a584-136">Figura 5: o</span><span class="sxs-lookup"><span data-stu-id="6a584-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="6a584-137">Passe o cursor do mouse sobre o resultado retornado, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **revelar no painel de elementos** para localizá-lo no dom ou **role para o modo de exibição para exibi** -lo na página.</span><span class="sxs-lookup"><span data-stu-id="6a584-137">Hover on the returned result, open the contextual menu \(right-click\), and select **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="6a584-138">Na figura a seguir, uma referência ao elemento atualmente selecionado é retornada e a propriedade src é exibida.</span><span class="sxs-lookup"><span data-stu-id="6a584-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$ (' Img '). src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="6a584-140">Figura 6: o</span><span class="sxs-lookup"><span data-stu-id="6a584-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="6a584-141">Esse método também dá suporte a um segundo parâmetro, startNode, que especifica um "elemento" ou um nó do qual Pesquisar elementos.</span><span class="sxs-lookup"><span data-stu-id="6a584-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="6a584-142">O valor padrão do parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="6a584-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="6a584-143">Na figura a seguir, o primeiro `img` elemento é encontrado após o `title--image` e exibe o `src` modo de exibição correto.</span><span class="sxs-lookup"><span data-stu-id="6a584-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ (' Img ', Document. querySelector (' título--imagem ')). src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="6a584-145">Figura 7: o</span><span class="sxs-lookup"><span data-stu-id="6a584-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6a584-146">Se você estiver usando uma biblioteca como o jQuery que usa `$` , a funcionalidade será sobrescrita e `$` corresponderá à implementação dessa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6a584-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="6a584-147">Seletor de consulta tudo</span><span class="sxs-lookup"><span data-stu-id="6a584-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="6a584-148">Retorna uma matriz de elementos que correspondem ao seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="6a584-149">Esse método é equivalente a chamar o método [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="6a584-149">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="6a584-150">No exemplo de código e na figura a seguir, use `$$()` para criar uma matriz de todos os `<img>` elementos no documento atual e exibir o valor da `src` propriedade de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="6a584-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Usando $ $ () para selecionar todas as imagens no documento e exibir as fontes" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="6a584-152">Figura 8: usar `$$()` para selecionar todas as imagens no documento e exibir as fontes</span><span class="sxs-lookup"><span data-stu-id="6a584-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-153">Esse método também oferece suporte a um segundo parâmetro, startNode, que especifica um elemento ou nó do qual Pesquisar elementos.</span><span class="sxs-lookup"><span data-stu-id="6a584-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="6a584-154">O valor padrão do parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="6a584-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="6a584-155">No exemplo de código e na figura a seguir, uma versão modificada do exemplo de código anterior e da figura usa `$$()` para criar uma matriz de todos os `<img>` elementos que aparecem no documento atual após o nó selecionado.</span><span class="sxs-lookup"><span data-stu-id="6a584-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usando $ $ () para selecionar todas as imagens que aparecem após o <div especificado> o elemento no documento e exibir as fontes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="6a584-157">Figura 9: usar `$$()` para selecionar todas as imagens que aparecem após o `<div>` elemento especificado no documento e exibir as fontes</span><span class="sxs-lookup"><span data-stu-id="6a584-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6a584-158">Pressione `Shift` + `Enter` no console para iniciar uma nova linha sem executar o script.</span><span class="sxs-lookup"><span data-stu-id="6a584-158">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="6a584-159">XPath</span><span class="sxs-lookup"><span data-stu-id="6a584-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="6a584-160">Retorna uma matriz de elementos DOM que correspondem à expressão XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="6a584-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="6a584-161">No exemplo de código e na figura a seguir, todos os `<p>` elementos na página são retornados.</span><span class="sxs-lookup"><span data-stu-id="6a584-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Usando um seletor XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="6a584-163">Figura 10: usando um seletor XPath</span><span class="sxs-lookup"><span data-stu-id="6a584-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-164">No exemplo de código e na figura a seguir, todos os `<p>` elementos que contêm `<a>` elementos são retornados.</span><span class="sxs-lookup"><span data-stu-id="6a584-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Usando um seletor XPath mais complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="6a584-166">Figura 11: usando um seletor XPath mais complicado</span><span class="sxs-lookup"><span data-stu-id="6a584-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-167">Semelhante aos outros comandos do seletor, `$x(path)` tem um segundo parâmetro opcional, `startNode` que especifica um elemento ou nó do qual Pesquisar elementos.</span><span class="sxs-lookup"><span data-stu-id="6a584-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Usando um seletor XPath com startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="6a584-169">Figura 12: usando um seletor XPath com</span><span class="sxs-lookup"><span data-stu-id="6a584-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <span data-ttu-id="6a584-170">elimina</span><span class="sxs-lookup"><span data-stu-id="6a584-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="6a584-171">Limpa o console do histórico.</span><span class="sxs-lookup"><span data-stu-id="6a584-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="6a584-172">copy</span><span class="sxs-lookup"><span data-stu-id="6a584-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="6a584-173">O `copy(object)` método copia uma representação de cadeia de caracteres do objeto especificado para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="6a584-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="6a584-174">depurar</span><span class="sxs-lookup"><span data-stu-id="6a584-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="6a584-175">O [problema Chromium #1050237][MonorailIssue1050237] está acompanhando um bug com a `debug()` função.</span><span class="sxs-lookup"><span data-stu-id="6a584-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="6a584-176">Se você tiver o problema, tente [usar pontos de interrupção][DevtoolsJavascriptBreakpoints] em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6a584-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="6a584-177">Quando você solicita o método especificado, o depurador é invocado e é quebrado dentro do método no painel **fontes** , permitindo que você percorra o código e depure-o.</span><span class="sxs-lookup"><span data-stu-id="6a584-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Quebrando dentro de um método com debug ()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="6a584-179">Figura 13: quebrando dentro de um método com</span><span class="sxs-lookup"><span data-stu-id="6a584-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="6a584-180">Use `undebug(method)` para parar de quebrar o método ou use a interface do usuário para desativar todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="6a584-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="6a584-181">Para obter mais informações sobre pontos de interrupção, consulte [Pausar um código com pontos de interrupção][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="6a584-181">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="6a584-182">dir</span><span class="sxs-lookup"><span data-stu-id="6a584-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="6a584-183">Exibe uma listagem de estilo de objeto de todas as propriedades do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="6a584-184">Esse método é um alias para o método [console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="6a584-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="6a584-185">Avaliar `document.head` no console para exibir o HTML entre as `<head>` marcas e `</head>` .</span><span class="sxs-lookup"><span data-stu-id="6a584-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="6a584-186">No exemplo de código e na imagem a seguir, uma listagem de estilo de objeto é exibida após `console.dir()` o uso no console.</span><span class="sxs-lookup"><span data-stu-id="6a584-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Registrando em log o documento. Head com o método dir ()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="6a584-188">Figura 14: registro `document.head` no `dir()` método</span><span class="sxs-lookup"><span data-stu-id="6a584-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-189">Para obter mais informações, consulte a [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrada na API do console.</span><span class="sxs-lookup"><span data-stu-id="6a584-189">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="6a584-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="6a584-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="6a584-191">Imprime uma representação XML do objeto especificado, como visto na guia **elementos** .  Esse método é equivalente ao método [console. DirXML ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="6a584-191">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="6a584-192">inspeção</span><span class="sxs-lookup"><span data-stu-id="6a584-192">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="6a584-193">Abre e seleciona o elemento ou o objeto especificado no painel apropriado: o painel **elementos** para elementos DOM ou o painel **memória** para objetos de heap JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6a584-193">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="6a584-194">No exemplo de código e na figura a seguir, o `document.body` abre no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="6a584-194">In the following code sample and figure, the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspecionar um elemento com inspeção ()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="6a584-196">Figura 15: inspecionar um elemento com</span><span class="sxs-lookup"><span data-stu-id="6a584-196">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="6a584-197">Ao passar um método para inspecionar, o método abre o documento no painel **fontes** para inspeção.</span><span class="sxs-lookup"><span data-stu-id="6a584-197">When passing a method to inspect, the method opens the document in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="6a584-198">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="6a584-198">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="6a584-199">Retorna os ouvintes de eventos registrados no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-199">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="6a584-200">O valor de retorno é um objeto que contém uma matriz para cada tipo de evento registrado \ (como `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="6a584-200">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="6a584-201">Os membros de cada matriz são objetos que descrevem o ouvinte registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="6a584-201">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="6a584-202">Na imagem de exemplo de código a seguir, todos os ouvintes de eventos registrados no objeto do documento são listados.</span><span class="sxs-lookup"><span data-stu-id="6a584-202">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Saída do uso de getEventListeners (documento)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="6a584-204">Figura 16: o resultado de usar</span><span class="sxs-lookup"><span data-stu-id="6a584-204">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="6a584-205">Se mais de um ouvinte estiver registrado no objeto especificado, a matriz contém um membro para cada ouvinte.</span><span class="sxs-lookup"><span data-stu-id="6a584-205">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="6a584-206">Na figura a seguir, há dois ouvintes de eventos registrados no elemento do documento para o `click` evento.</span><span class="sxs-lookup"><span data-stu-id="6a584-206">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Vários ouvintes" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="6a584-208">Figura 17: vários ouvintes</span><span class="sxs-lookup"><span data-stu-id="6a584-208">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-209">Você pode expandir ainda mais cada um dos seguintes objetos para explorar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="6a584-209">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Exibição expandida do objeto Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="6a584-211">Figura 18: exibição expandida do objeto Listener</span><span class="sxs-lookup"><span data-stu-id="6a584-211">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <span data-ttu-id="6a584-212">chaves</span><span class="sxs-lookup"><span data-stu-id="6a584-212">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="6a584-213">Retorna uma matriz que contém os nomes das propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-213">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="6a584-214">Para obter os valores associados das mesmas propriedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="6a584-214">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="6a584-215">Por exemplo, suponha que seu aplicativo definiu o objeto a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a584-215">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="6a584-216">Nos exemplos de código e na figura a seguir, o resultado pressupõe `player1` que foi definido no namespace global \ (para simplicidade \) antes de digitar `keys(player1)` e `values(player1)` no console.</span><span class="sxs-lookup"><span data-stu-id="6a584-216">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Os comandos Keys () e Values ()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="6a584-218">Figura 19: `keys()` comandos e `values()`</span><span class="sxs-lookup"><span data-stu-id="6a584-218">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <span data-ttu-id="6a584-219">monitor</span><span class="sxs-lookup"><span data-stu-id="6a584-219">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="6a584-220">Registra uma mensagem no console que indica o nome do método juntamente com os argumentos que são passados para o método quando ele é chamado.</span><span class="sxs-lookup"><span data-stu-id="6a584-220">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="O método monitor ()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="6a584-222">Figura 20: o `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="6a584-222">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-223">Use `unmonitor(method)` para interromper o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="6a584-223">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="6a584-224">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="6a584-224">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="6a584-225">Quando ocorre um dos eventos especificados no objeto especificado, o objeto de evento é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="6a584-225">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="6a584-226">Você pode especificar um único evento para monitorar, uma matriz de eventos ou um dos tipos de eventos genéricos que são mapeados para uma coleção predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a584-226">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="6a584-227">Consulte o exemplo de código e a imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a584-227">See the following code sample and figure.</span></span>  

<span data-ttu-id="6a584-228">Os seguintes monitores redimensionam eventos no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="6a584-228">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Janela de monitoramento redimensionar eventos" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="6a584-230">Figura 21: monitorar eventos do Window Resize</span><span class="sxs-lookup"><span data-stu-id="6a584-230">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="6a584-231">O seguinte define uma matriz para monitorar os dois `resize` e os `scroll` eventos no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="6a584-231">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="6a584-232">Você também pode especificar um dos tipos de eventos disponíveis, cadeias de caracteres que são mapeados para conjuntos de eventos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="6a584-232">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="6a584-233">A tabela a seguir mostra os tipos de eventos disponíveis e os mapeamentos de eventos associados.</span><span class="sxs-lookup"><span data-stu-id="6a584-233">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="6a584-234">Event type</span><span class="sxs-lookup"><span data-stu-id="6a584-234">Event type</span></span> | <span data-ttu-id="6a584-235">Eventos mapeados correspondentes</span><span class="sxs-lookup"><span data-stu-id="6a584-235">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="6a584-236">"clique em", "DblClick", "botão de mouse", "MouseUp", "mouseout", "mouse pressionado", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="6a584-236">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="6a584-237">"KeyDown", "KeyPress", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="6a584-237">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="6a584-238">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="6a584-238">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="6a584-239">"Blur", "alterar", "enfocar", "selecionar", "enviar", "zoom", "selecionar", "enviar", "zoom"</span><span class="sxs-lookup"><span data-stu-id="6a584-239">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="6a584-240">No exemplo de código a seguir, o `key` tipo de evento correspondente a `key` eventos em um campo de texto de entrada está selecionado atualmente no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="6a584-240">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="6a584-241">Na figura a seguir, a saída de exemplo após a digitação de um caractere no campo de texto é exibida.</span><span class="sxs-lookup"><span data-stu-id="6a584-241">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Monitorar eventos chave" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="6a584-243">Figura 22: monitorar eventos de chave</span><span class="sxs-lookup"><span data-stu-id="6a584-243">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <span data-ttu-id="6a584-244">profile</span><span class="sxs-lookup"><span data-stu-id="6a584-244">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="6a584-245">Inicia uma sessão de criação de perfil de CPU JavaScript com um nome opcional.</span><span class="sxs-lookup"><span data-stu-id="6a584-245">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="6a584-246">O método [profileEnd ()](#profileend) conclui o perfil e exibe os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="6a584-246">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="6a584-247">Execute o `profile()` método para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="6a584-247">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="6a584-248">Execute o método [profileEnd ()](#profileend) para interromper a criação de perfil e exibir os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="6a584-248">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="6a584-249">Perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="6a584-249">Profiles may also be nested.</span></span>  <span data-ttu-id="6a584-250">Nos exemplos de código a seguir, configurando o resultado é o mesmo, independentemente da ordem.</span><span class="sxs-lookup"><span data-stu-id="6a584-250">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="6a584-251">Vários perfis de CPU podem operar ao mesmo tempo e não é necessário fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="6a584-251">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="6a584-252">profileEnd</span><span class="sxs-lookup"><span data-stu-id="6a584-252">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="6a584-253">Conclui uma sessão de criação de perfil de CPU JavaScript e exibe os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="6a584-253">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="6a584-254">Você deve estar executando o método [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="6a584-254">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="6a584-255">Execute o método [Profile ()](#profile) para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="6a584-255">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="6a584-256">Execute o `profileEnd()` método para interromper a criação de perfil e exibir os resultados no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="6a584-256">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="6a584-257">Perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="6a584-257">Profiles may also be nested.</span></span>  <span data-ttu-id="6a584-258">No exemplo de código a seguir e figura, o resultado é o mesmo, independentemente da ordem.</span><span class="sxs-lookup"><span data-stu-id="6a584-258">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="6a584-259">O resultado aparece como um instantâneo de heap no painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="6a584-259">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfis agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="6a584-261">Figura 23: perfis agrupados</span><span class="sxs-lookup"><span data-stu-id="6a584-261">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6a584-262">Vários perfis de CPU podem operar ao mesmo tempo e não é necessário fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="6a584-262">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="6a584-263">queryObjects</span><span class="sxs-lookup"><span data-stu-id="6a584-263">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="6a584-264">Retorna uma matriz de objetos criados com o Construtor especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-264">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="6a584-265">O escopo de `queryObjects()` é o contexto de tempo de execução atualmente selecionado no console.</span><span class="sxs-lookup"><span data-stu-id="6a584-265">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="6a584-266">Retorna All `Promises` .</span><span class="sxs-lookup"><span data-stu-id="6a584-266">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="6a584-267">Retorna todos os elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="6a584-267">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="6a584-268">Retorna todos os objetos que foram instanciados usando `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="6a584-268">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <span data-ttu-id="6a584-269">TableName</span><span class="sxs-lookup"><span data-stu-id="6a584-269">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="6a584-270">Registra dados de objeto com formatação de tabela com base no objeto de dados em títulos de coluna opcionais.</span><span class="sxs-lookup"><span data-stu-id="6a584-270">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="6a584-271">No exemplo de código e na imagem a seguir, é exibida uma lista de nomes usando uma tabela no console.</span><span class="sxs-lookup"><span data-stu-id="6a584-271">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="O resultado do método Table ()" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="6a584-273">Figura 24: o resultado do `table()` método</span><span class="sxs-lookup"><span data-stu-id="6a584-273">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <span data-ttu-id="6a584-274">desdepurar</span><span class="sxs-lookup"><span data-stu-id="6a584-274">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="6a584-275">Interrompe a depuração do método especificado para que, quando o método for chamado, o depurador não seja mais invocado.</span><span class="sxs-lookup"><span data-stu-id="6a584-275">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="6a584-276">desmonitorar</span><span class="sxs-lookup"><span data-stu-id="6a584-276">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="6a584-277">Interrompe o monitoramento do método especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-277">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="6a584-278">Esse método é usado em conjunto com o método [Monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="6a584-278">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="6a584-279">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="6a584-279">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="6a584-280">Interrompe o monitoramento de eventos do objeto e dos eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="6a584-280">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="6a584-281">Por exemplo, o seguinte interrompe todos os monitoramentos de evento no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="6a584-281">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="6a584-282">Você também pode parar seletivamente o monitoramento de eventos específicos em um objeto.</span><span class="sxs-lookup"><span data-stu-id="6a584-282">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="6a584-283">Por exemplo, o código a seguir começa a monitorar todos os `mouse` eventos no elemento atualmente selecionado e, em seguida, interrompe o monitoramento de `mousemove` eventos \ (talvez reduzir o ruído na saída do console \).</span><span class="sxs-lookup"><span data-stu-id="6a584-283">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="6a584-284">valores</span><span class="sxs-lookup"><span data-stu-id="6a584-284">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="6a584-285">Retorna uma matriz que contém os valores de todas as propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="6a584-285">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

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
> <span data-ttu-id="6a584-295">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="6a584-295">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6a584-296">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/utilities) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6a584-296">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6a584-298">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a584-298">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
