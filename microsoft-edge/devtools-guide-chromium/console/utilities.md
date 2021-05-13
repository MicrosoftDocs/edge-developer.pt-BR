---
description: Uma referência de comandos de conveniência disponíveis no console Microsoft Edge DevTools.
title: Referência de API de Utilitários do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 436f2807c5fab1723ca6cc93fddc68d9ecf12db7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564529"
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
# <a name="console-utilities-api-reference"></a><span data-ttu-id="958c5-104">Referência de API de Utilitários do console</span><span class="sxs-lookup"><span data-stu-id="958c5-104">Console Utilities API reference</span></span>  

<span data-ttu-id="958c5-105">A API Utilitários de Console contém uma coleção de comandos de conveniência para concluir as seguintes tarefas comuns.</span><span class="sxs-lookup"><span data-stu-id="958c5-105">The Console Utilities API contains a collection of convenience commands to complete the following common tasks.</span></span>  

*   <span data-ttu-id="958c5-106">Escolher e inspecionar elementos DOM</span><span class="sxs-lookup"><span data-stu-id="958c5-106">Choose and inspect DOM elements</span></span>  
*   <span data-ttu-id="958c5-107">Exibir dados em formato acessível</span><span class="sxs-lookup"><span data-stu-id="958c5-107">Display data in readable format</span></span>  
*   <span data-ttu-id="958c5-108">Parar e iniciar o profiler</span><span class="sxs-lookup"><span data-stu-id="958c5-108">Stop and start the profiler</span></span>  
*   <span data-ttu-id="958c5-109">Monitorar eventos DOM</span><span class="sxs-lookup"><span data-stu-id="958c5-109">Monitor DOM events</span></span>  
    
> [!WARNING]
> <span data-ttu-id="958c5-110">Os comandos a seguir só funcionam no console \*\*\*\* Microsoft Edge DevTools .</span><span class="sxs-lookup"><span data-stu-id="958c5-110">The following commands only work in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="958c5-111">Os comandos não funcionarão se executados de seus scripts.</span><span class="sxs-lookup"><span data-stu-id="958c5-111">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="958c5-112">Para obter mais informações sobre os métodos e e o restante dos `console.log()` `console.error()` `console.*` métodos, navegue até [Console API Reference][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="958c5-112">For more information about the `console.log()` and `console.error()` methods and the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="958c5-113">Expressão avaliada recentemente</span><span class="sxs-lookup"><span data-stu-id="958c5-113">Recently evaluated expression</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-114">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-114">Console syntax</span></span>  

```console
$_
```  

<span data-ttu-id="958c5-115">Este comando retorna o valor da expressão avaliada mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="958c5-115">This command returns the value of the most recently evaluated expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-116">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-116">Console example</span></span>  

<span data-ttu-id="958c5-117">Na figura a seguir, uma expressão simples \( `2 + 2` \) é avaliada.</span><span class="sxs-lookup"><span data-stu-id="958c5-117">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="958c5-118">Em `$_` seguida, a propriedade é avaliada, que contém o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="958c5-118">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ é a expressão avaliada mais recentemente" lightbox="../media/console-arithmatic.msft.png":::
   `$_` <span data-ttu-id="958c5-120">é a expressão avaliada mais recentemente</span><span class="sxs-lookup"><span data-stu-id="958c5-120">is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-121">Na figura a seguir, a expressão avaliada inicialmente contém uma matriz de nomes.</span><span class="sxs-lookup"><span data-stu-id="958c5-121">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="958c5-122">Avaliando para encontrar o comprimento da matriz, o valor armazenado se torna a expressão avaliada mais `$_.length` `$_` recente, `4` .</span><span class="sxs-lookup"><span data-stu-id="958c5-122">Evaluating `$_.length` to find the length of the array, the value stored in `$_` becomes the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ muda quando novos comandos são avaliados" lightbox="../media/console-array-length.msft.png":::
   `$_` <span data-ttu-id="958c5-124">muda quando novos comandos são avaliados</span><span class="sxs-lookup"><span data-stu-id="958c5-124">changes when new commands are evaluated</span></span>  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="958c5-125">Elemento escolhido recentemente ou objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="958c5-125">Recently chosen element or JavaScript object</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-126">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-126">Console syntax</span></span>  

```console
$0
```  

<span data-ttu-id="958c5-127">Este comando retorna o elemento escolhido mais recentemente ou o objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="958c5-127">This command returns the most recently chosen element or JavaScript object.</span></span>  `$1` <span data-ttu-id="958c5-128">retorna o segundo escolhido mais recentemente e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="958c5-128">returns the second most recently chosen one, and so on.</span></span>  <span data-ttu-id="958c5-129">Os comandos , , e funcionam como uma referência histórica aos últimos cinco elementos DOM inspecionados na ferramenta Elements ou os cinco últimos objetos de pilha JavaScript escolhidos na `$0` `$1` ferramenta `$2` `$3` `$4` **Memória.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="958c5-129">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects chosen in the **Memory** tool.</span></span>  

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
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a><span data-ttu-id="958c5-130">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-130">Console example</span></span>  

<span data-ttu-id="958c5-131">Na figura a seguir, um `img` elemento é escolhido na ferramenta **Elements.**</span><span class="sxs-lookup"><span data-stu-id="958c5-131">In the following figure, an `img` element is chosen in the **Elements** tool.</span></span>  <span data-ttu-id="958c5-132">Na gaveta **Console,** `$0` foi avaliado e exibe o mesmo elemento.</span><span class="sxs-lookup"><span data-stu-id="958c5-132">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Os $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="958c5-134">O</span><span class="sxs-lookup"><span data-stu-id="958c5-134">The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="958c5-135">Na figura a seguir, a imagem exibe um elemento diferente escolhido na mesma página da Web.</span><span class="sxs-lookup"><span data-stu-id="958c5-135">In the following figure, the image displays a different element chosen in the same webpage.</span></span>  <span data-ttu-id="958c5-136">O `$0` agora se refere ao elemento recém-escolhido, enquanto retorna o escolhido `$1` anteriormente.</span><span class="sxs-lookup"><span data-stu-id="958c5-136">The `$0` now refers to the newly chosen element, while `$1` returns the previously chosen one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="O $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="958c5-138">O</span><span class="sxs-lookup"><span data-stu-id="958c5-138">The</span></span> `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a><span data-ttu-id="958c5-139">Seletor de consulta</span><span class="sxs-lookup"><span data-stu-id="958c5-139">Query selector</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-140">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-140">Console syntax</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="958c5-141">Este comando retorna a referência ao primeiro elemento DOM com o seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-141">This command returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="958c5-142">Este método é um alias para o [método document.querySelector().][MdnDocsWebApiDocumentQueryselector]</span><span class="sxs-lookup"><span data-stu-id="958c5-142">This method is an alias for the [document.querySelector()][MdnDocsWebApiDocumentQueryselector] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-143">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-143">Console example</span></span>  

<span data-ttu-id="958c5-144">Na figura a seguir, uma referência ao primeiro `<img>` elemento na página da Web é retornada.</span><span class="sxs-lookup"><span data-stu-id="958c5-144">In the following figure, a reference to the first `<img>` element in the webpage is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="958c5-146">O</span><span class="sxs-lookup"><span data-stu-id="958c5-146">The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="958c5-147">Para encontrar o primeiro elemento no DOM ou para encontrá-lo e exibi-lo na página da Web, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="958c5-147">To find the first element in the DOM or to find and display it on the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="958c5-148">Passe o mouse no resultado retornado.</span><span class="sxs-lookup"><span data-stu-id="958c5-148">Hover on the returned result.</span></span>  
1.  <span data-ttu-id="958c5-149">Abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="958c5-149">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="958c5-150">Escolha **Revelar no Painel de Elementos**.</span><span class="sxs-lookup"><span data-stu-id="958c5-150">Choose **Reveal in Elements Panel**.</span></span>  

<span data-ttu-id="958c5-151">Na figura a seguir, uma referência ao elemento escolhido no momento é retornada e a `src` propriedade é exibida.</span><span class="sxs-lookup"><span data-stu-id="958c5-151">In the following figure, a reference to the currently chosen element is returned and the `src` property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="958c5-153">O</span><span class="sxs-lookup"><span data-stu-id="958c5-153">The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="958c5-154">Este método também dá suporte a um segundo parâmetro, , que especifica um elemento ou nó do qual `startNode` procurar elementos.</span><span class="sxs-lookup"><span data-stu-id="958c5-154">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="958c5-155">O valor padrão do parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="958c5-155">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="958c5-156">Na figura a seguir, o primeiro elemento após o elemento é encontrado e a `img` propriedade do elemento é `title--image` `src` `img` retornada.</span><span class="sxs-lookup"><span data-stu-id="958c5-156">In the following figure, the first `img` element after the `title--image` element is found, and the `src` property of the `img` element is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="958c5-158">O</span><span class="sxs-lookup"><span data-stu-id="958c5-158">The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="958c5-159">Se você estiver usando uma biblioteca como jQuery que usa , a funcionalidade será substituída e corresponderá à implementação `$` `$` dessa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="958c5-159">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

---  

## <a name="query-selector-all"></a><span data-ttu-id="958c5-160">Seletor de consulta todos</span><span class="sxs-lookup"><span data-stu-id="958c5-160">Query selector all</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-161">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-161">Console syntax</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="958c5-162">Este comando retorna uma matriz de elementos que corresponderão ao seletor CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-162">This command returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="958c5-163">Esse método equivale a executar o [método document.querySelectorAll().][MdnDocsWebApiDocumentQueryselectorall]</span><span class="sxs-lookup"><span data-stu-id="958c5-163">This method is equivalent to running the [document.querySelectorAll()][MdnDocsWebApiDocumentQueryselectorall] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-164">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-164">Console example</span></span>  

<span data-ttu-id="958c5-165">Na figura e exemplo de código a seguir, use para criar uma matriz de todos os elementos na página da Web atual e exibir o valor da propriedade `$$()` `<img>` para cada `src` elemento.</span><span class="sxs-lookup"><span data-stu-id="958c5-165">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current webpage and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Usando $$() para escolher todas as imagens na página da Web e exibir as fontes" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="958c5-167">Usando `$$()` para escolher todas as imagens na página da Web e exibir as fontes</span><span class="sxs-lookup"><span data-stu-id="958c5-167">Using `$$()` to choose all images in the webpage and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-168">Este método também dá suporte a um segundo parâmetro, , que especifica um elemento ou nó do qual `startNode` procurar elementos.</span><span class="sxs-lookup"><span data-stu-id="958c5-168">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="958c5-169">O valor padrão do parâmetro é `document` .</span><span class="sxs-lookup"><span data-stu-id="958c5-169">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="958c5-170">Na figura e amostra de código a seguir, uma versão modificada do exemplo de código anterior e a figura usam para criar uma matriz de todos os elementos que aparecem na página da Web atual após o `$$()` `<img>` nó escolhido.</span><span class="sxs-lookup"><span data-stu-id="958c5-170">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current webpage after the chosen node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usando $$() para escolher todas as imagens que aparecem após o elemento div <div> na página da Web e exibir as fontes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="958c5-172">Usando `$$()` para escolher todas as imagens que aparecem após o elemento especificado na página da Web e exibir as `<div>` fontes</span><span class="sxs-lookup"><span data-stu-id="958c5-172">Using `$$()` to choose all images that appear after the specified `<div>` element in the webpage and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="958c5-173">Selecione `Shift` + `Enter` no **Console para** iniciar uma nova linha sem executar o script.</span><span class="sxs-lookup"><span data-stu-id="958c5-173">Select `Shift`+`Enter` in the **Console** to start a new line without running the script.</span></span>  

---  

## <a name="xpath"></a><span data-ttu-id="958c5-174">XPath</span><span class="sxs-lookup"><span data-stu-id="958c5-174">XPath</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-175">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-175">Console syntax</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="958c5-176">Este comando retorna uma matriz de elementos DOM que combinam com a expressão XPath especificada.</span><span class="sxs-lookup"><span data-stu-id="958c5-176">This command returns an array of DOM elements that match the specified XPath expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-177">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-177">Console example</span></span>  

<span data-ttu-id="958c5-178">Na figura e no exemplo de código a seguir, todos os `<p>` elementos na página da Web são retornados.</span><span class="sxs-lookup"><span data-stu-id="958c5-178">In the following code sample and figure, all of the `<p>` elements on the webpage are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Usando um seletor XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="958c5-180">Usando um seletor XPath</span><span class="sxs-lookup"><span data-stu-id="958c5-180">Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-181">Na figura e amostra de código a seguir, todos os `<p>` elementos que contêm `<a>` elementos são retornados.</span><span class="sxs-lookup"><span data-stu-id="958c5-181">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Usando um seletor XPath mais complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="958c5-183">Usando um seletor XPath mais complicado</span><span class="sxs-lookup"><span data-stu-id="958c5-183">Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-184">Semelhante aos outros comandos do seletor, tem um segundo parâmetro opcional, , que especifica um elemento ou nó do qual `$x(path)` `startNode` procurar elementos.</span><span class="sxs-lookup"><span data-stu-id="958c5-184">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Usando um seletor XPath com startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="958c5-186">Usando um seletor XPath com</span><span class="sxs-lookup"><span data-stu-id="958c5-186">Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="958c5-187">clear</span><span class="sxs-lookup"><span data-stu-id="958c5-187">clear</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-188">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-188">Console syntax</span></span>  

```console
clear()
```  

<span data-ttu-id="958c5-189">Essa vírgula limpa o console do histórico.</span><span class="sxs-lookup"><span data-stu-id="958c5-189">This commnad clears the console of the history.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-190">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-190">Console example</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="958c5-191">copy</span><span class="sxs-lookup"><span data-stu-id="958c5-191">copy</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-192">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-192">Console syntax</span></span>  

```console
copy(object)
```  

<span data-ttu-id="958c5-193">Este método copia uma representação de cadeia de caracteres do objeto especificado para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="958c5-193">This method copies a string representation of the specified object to the clipboard.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-194">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-194">Console example</span></span>  

```console
copy($0)
```  

---  

## <a name="debug"></a><span data-ttu-id="958c5-195">depurar</span><span class="sxs-lookup"><span data-stu-id="958c5-195">debug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-196">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-196">Console syntax</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="958c5-197">O [Chromium problema #1050237][CR1050237] está rastreando um bug com a `debug()` função.</span><span class="sxs-lookup"><span data-stu-id="958c5-197">The [Chromium issue #1050237][CR1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="958c5-198">Se você encontrar o problema, tente usar [pontos de interrupção.][DevtoolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="958c5-198">If you encounter the issue, try using [breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="958c5-199">Quando você solicita o método especificado, o depurador invoca e quebra dentro do método na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="958c5-199">When you request the specified method, the debugger invokes and breaks inside the method on the **Sources** tool.</span></span>  <span data-ttu-id="958c5-200">Ele permite que você passo a passo e depurar o código.</span><span class="sxs-lookup"><span data-stu-id="958c5-200">It allows you to step through and debug the code.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-201">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-201">Console example</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Quebrar dentro de um método com depuração()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="958c5-203">Quebrar dentro de um método com</span><span class="sxs-lookup"><span data-stu-id="958c5-203">Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="958c5-204">Use para parar de quebrar o método ou use a interface do usuário `undebug(method)` para desativar todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="958c5-204">Use `undebug(method)` to stop breaking on the method, or use the UI to turn off all breakpoints.</span></span>  

<span data-ttu-id="958c5-205">Para obter mais informações sobre pontos de interrupção, navegue até [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="958c5-205">For more information on breakpoints, navigate to [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span></span>  

---  

## <a name="dir"></a><span data-ttu-id="958c5-206">dir</span><span class="sxs-lookup"><span data-stu-id="958c5-206">dir</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-207">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-207">Console syntax</span></span>  

```console
dir(object)
```  

<span data-ttu-id="958c5-208">Este comando exibe uma listagem de estilo de objeto de todas as propriedades do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-208">This command displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="958c5-209">Este método é um alias para o [método console.dir().][MdnDocsWebApiConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="958c5-209">This method is an alias for the [console.dir()][MdnDocsWebApiConsoleDir] method.</span></span>  

<span data-ttu-id="958c5-210">Avalie `document.head` no Console **para** exibir o HTML entre as `<head>` marcas `</head>` e.</span><span class="sxs-lookup"><span data-stu-id="958c5-210">Evaluate `document.head` in the **Console** to display the HTML between the `<head>` and `</head>` tags.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-211">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-211">Console example</span></span>  

<span data-ttu-id="958c5-212">Na figura e exemplo de código a seguir, uma listagem de estilo de objeto é exibida após o uso `console.dir()` no **Console**.</span><span class="sxs-lookup"><span data-stu-id="958c5-212">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the **Console**.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Método log document.head com dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="958c5-214">Log `document.head` com `dir()` método</span><span class="sxs-lookup"><span data-stu-id="958c5-214">Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-215">Para obter mais informações, [navegue até console.dir()][DevToolsConsoleApiConsoleDirObject] na API do Console.</span><span class="sxs-lookup"><span data-stu-id="958c5-215">For more information, navigate to [console.dir()][DevToolsConsoleApiConsoleDirObject] in the Console API.</span></span>  

---  

## <a name="dirxml"></a><span data-ttu-id="958c5-216">dirxml</span><span class="sxs-lookup"><span data-stu-id="958c5-216">dirxml</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-217">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-217">Console syntax</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="958c5-218">Este comando imprime uma representação XML do objeto especificado, conforme exibido na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="958c5-218">This command prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="958c5-219">Esse método é equivalente ao [método console.dirxml().][MdnDocsWebApiConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="958c5-219">This method is equivalent to the [console.dirxml()][MdnDocsWebApiConsoleDirxml] method.</span></span>  

---  

## <a name="inspect"></a><span data-ttu-id="958c5-220">inspect</span><span class="sxs-lookup"><span data-stu-id="958c5-220">inspect</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-221">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-221">Console syntax</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="958c5-222">Este comando abre e escolhe o elemento ou objeto especificado no painel apropriado: a ferramenta **Elements** para elementos DOM ou a ferramenta **Memória** para objetos de pilha JavaScript.</span><span class="sxs-lookup"><span data-stu-id="958c5-222">This command opens and chooses the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-223">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-223">Console example</span></span>  

<span data-ttu-id="958c5-224">Na figura e amostra de código a seguir, a `document.body` abre na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="958c5-224">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-225">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-225">Console example</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspecionar um elemento com inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="958c5-227">Inspecionar um elemento com</span><span class="sxs-lookup"><span data-stu-id="958c5-227">Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="958c5-228">Ao passar um método a ser inspecionado, o método abre a página da Web na **ferramenta Fontes** para você inspecionar.</span><span class="sxs-lookup"><span data-stu-id="958c5-228">When passing a method to inspect, the method opens the webpage in the **Sources** tool for you to inspect.</span></span>  

---  

## <a name="geteventlisteners"></a><span data-ttu-id="958c5-229">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="958c5-229">getEventListeners</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-230">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-230">Console syntax</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="958c5-231">Este comando retorna os ouvintes de eventos registrados no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-231">This command returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="958c5-232">O valor de retorno é um objeto que contém uma matriz para cada tipo de evento registrado \(como `click` ou `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="958c5-232">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="958c5-233">Os membros de cada matriz são objetos que descrevem o ouvinte registrado para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="958c5-233">The members of each array are objects that describe the listener registered for each type.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-234">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-234">Console example</span></span>  

<span data-ttu-id="958c5-235">No trecho de código a seguir e na figura, todos os ouvintes de eventos registrados no `document` objeto são listados.</span><span class="sxs-lookup"><span data-stu-id="958c5-235">In the following code snippet and figure, all of the event listeners registered on the `document` object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Saída do uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="958c5-237">O resultado do uso</span><span class="sxs-lookup"><span data-stu-id="958c5-237">The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="958c5-238">Se mais de um ouvinte estiver registrado no objeto especificado, a matriz conterá um membro para cada ouvinte.</span><span class="sxs-lookup"><span data-stu-id="958c5-238">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="958c5-239">Na figura a seguir, dois ouvintes de eventos são registrados no `document` elemento do `click` evento.</span><span class="sxs-lookup"><span data-stu-id="958c5-239">In the following figure, two event listeners are registered on the `document` element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Vários ouvintes" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="958c5-241">Vários ouvintes</span><span class="sxs-lookup"><span data-stu-id="958c5-241">Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-242">Você pode expandir ainda mais cada um dos objetos a seguir para explorar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="958c5-242">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Exibição expandida do objeto ouvinte" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="958c5-244">Exibição expandida do objeto ouvinte</span><span class="sxs-lookup"><span data-stu-id="958c5-244">Expanded view of listener object</span></span>  
:::image-end:::  

---  

## <a name="keys"></a><span data-ttu-id="958c5-245">chaves</span><span class="sxs-lookup"><span data-stu-id="958c5-245">keys</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-246">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-246">Console syntax</span></span>  

```console
keys(object)
```  

<span data-ttu-id="958c5-247">Este comando retorna uma matriz que contém os nomes das propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-247">This command returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="958c5-248">Para obter os valores associados das mesmas propriedades, use `values()` .</span><span class="sxs-lookup"><span data-stu-id="958c5-248">To get the associated values of the same properties, use `values()`.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-249">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-249">Console example</span></span>  

<span data-ttu-id="958c5-250">Por exemplo, suponha que seu aplicativo definiu o objeto a seguir.</span><span class="sxs-lookup"><span data-stu-id="958c5-250">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = {"name": "Ted", "level": 42}
```  

<span data-ttu-id="958c5-251">Na figura e amostras de código a seguir, o resultado supõe que foi definido no `player1` namespace global \(for simplicity\) antes de digitar e `keys(player1)` no `values(player1)` console.</span><span class="sxs-lookup"><span data-stu-id="958c5-251">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) before you type `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Os comandos keys() e values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="958c5-253">Comandos `keys()` e `values()`</span><span class="sxs-lookup"><span data-stu-id="958c5-253">The `keys()` and `values()` commands</span></span>  
:::image-end:::  

---  

## <a name="monitor"></a><span data-ttu-id="958c5-254">monitor</span><span class="sxs-lookup"><span data-stu-id="958c5-254">monitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-255">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-255">Console syntax</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="958c5-256">Esse comando registra uma mensagem no console que indica o nome do método juntamente com os argumentos passados para o método como parte de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="958c5-256">This command logs a message to the console that indicates the method name along with the arguments passed to the method as part of a request.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-257">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-257">Console example</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="O método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="958c5-259">O `monitor()` método</span><span class="sxs-lookup"><span data-stu-id="958c5-259">The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-260">Use `unmonitor(method)` para encerrar o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="958c5-260">Use `unmonitor(method)` to end monitoring.</span></span>  

---  

## <a name="monitorevents"></a><span data-ttu-id="958c5-261">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="958c5-261">monitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-262">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-262">Console syntax</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="958c5-263">Quando um dos eventos especificados ocorre no objeto especificado, o objeto de evento é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="958c5-263">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="958c5-264">Você pode especificar um único evento a ser monitorado, uma matriz de eventos ou um dos tipos de eventos genéricos mapeados para uma coleção predefinida de eventos.</span><span class="sxs-lookup"><span data-stu-id="958c5-264">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-265">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-265">Console example</span></span>  

<span data-ttu-id="958c5-266">Revise o exemplo de código a seguir e a figura.</span><span class="sxs-lookup"><span data-stu-id="958c5-266">Review the following code sample and figure.</span></span>  

<span data-ttu-id="958c5-267">O seguinte monitora todos os eventos de resize no objeto window.</span><span class="sxs-lookup"><span data-stu-id="958c5-267">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Monitoring window resize events" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="958c5-269">Monitoring window resize events</span><span class="sxs-lookup"><span data-stu-id="958c5-269">Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="958c5-270">O trecho de código a seguir define uma matriz para monitorar eventos e eventos `resize` `scroll` no objeto window.</span><span class="sxs-lookup"><span data-stu-id="958c5-270">The following code snippet defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="958c5-271">Você também pode especificar um dos tipos de eventos disponíveis, cadeias de caracteres que mapeiam para conjuntos predefinidos de eventos.</span><span class="sxs-lookup"><span data-stu-id="958c5-271">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="958c5-272">A tabela a seguir exibe os tipos de eventos disponíveis e os mapeamentos de eventos associados.</span><span class="sxs-lookup"><span data-stu-id="958c5-272">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="958c5-273">Event type</span><span class="sxs-lookup"><span data-stu-id="958c5-273">Event type</span></span> | <span data-ttu-id="958c5-274">Eventos mapeados correspondentes</span><span class="sxs-lookup"><span data-stu-id="958c5-274">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="958c5-275">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span><span class="sxs-lookup"><span data-stu-id="958c5-275">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="958c5-276">"keydown", "keypress", "keyup", "textInput"</span><span class="sxs-lookup"><span data-stu-id="958c5-276">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="958c5-277">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="958c5-277">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="958c5-278">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span><span class="sxs-lookup"><span data-stu-id="958c5-278">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="958c5-279">No exemplo de código a seguir, o tipo de evento correspondente a eventos em um campo de texto de entrada é escolhido `key` `key` atualmente na ferramenta **Elements.**</span><span class="sxs-lookup"><span data-stu-id="958c5-279">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently chosen in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="958c5-280">Na figura a seguir, a saída de exemplo após digitar um caractere no campo de texto é exibida.</span><span class="sxs-lookup"><span data-stu-id="958c5-280">In the following figure, the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Monitorando os principais eventos" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="958c5-282">Monitorando os principais eventos</span><span class="sxs-lookup"><span data-stu-id="958c5-282">Monitoring key events</span></span>  
:::image-end:::  

---  

## <a name="profile"></a><span data-ttu-id="958c5-283">profile</span><span class="sxs-lookup"><span data-stu-id="958c5-283">profile</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-284">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-284">Console syntax</span></span>  

```console
profile([name])
```  

<span data-ttu-id="958c5-285">Este comando inicia uma sessão de criação de perfil de CPU JavaScript com um nome opcional.</span><span class="sxs-lookup"><span data-stu-id="958c5-285">This command starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="958c5-286">O [método profileEnd()](#profileend) conclui o perfil e exibe os resultados na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="958c5-286">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="958c5-287">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-287">Console example</span></span>  

1.  <span data-ttu-id="958c5-288">Execute o `profile()` método para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="958c5-288">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="958c5-289">Execute o [método profileEnd()](#profileend) para interromper a criação de perfil e exibir os resultados na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="958c5-289">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="958c5-290">Os perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="958c5-290">Profiles may also be nested.</span></span>  <span data-ttu-id="958c5-291">Na figura e amostras de código a seguir, o resultado é o mesmo, seja qual for a ordem.</span><span class="sxs-lookup"><span data-stu-id="958c5-291">In the following code samples and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="958c5-292">Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="958c5-292">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="profileend"></a><span data-ttu-id="958c5-293">profileEnd</span><span class="sxs-lookup"><span data-stu-id="958c5-293">profileEnd</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-294">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-294">Console syntax</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="958c5-295">Este comando conclui uma sessão de criação de perfil de CPU JavaScript e exibe os resultados na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="958c5-295">This command completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="958c5-296">Você deve estar executando o [método profile().](#profile)</span><span class="sxs-lookup"><span data-stu-id="958c5-296">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="958c5-297">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-297">Console example</span></span>  

1.  <span data-ttu-id="958c5-298">Execute o [método profile()](#profile) para iniciar a criação de perfil.</span><span class="sxs-lookup"><span data-stu-id="958c5-298">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="958c5-299">Execute o `profileEnd()` método para interromper a criação de perfil e exibir os resultados na ferramenta **Memória.**</span><span class="sxs-lookup"><span data-stu-id="958c5-299">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="958c5-300">Os perfis também podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="958c5-300">Profiles may also be nested.</span></span>  <span data-ttu-id="958c5-301">Na figura e amostra de código a seguir, o resultado é o mesmo, seja qual for a ordem.</span><span class="sxs-lookup"><span data-stu-id="958c5-301">In the following code sample and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="958c5-302">O resultado aparece como um Instantâneo de Pilha na **ferramenta Memória.**</span><span class="sxs-lookup"><span data-stu-id="958c5-302">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfis agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="958c5-304">Perfis agrupados</span><span class="sxs-lookup"><span data-stu-id="958c5-304">Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="958c5-305">Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="958c5-305">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="queryobjects"></a><span data-ttu-id="958c5-306">queryObjects</span><span class="sxs-lookup"><span data-stu-id="958c5-306">queryObjects</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-307">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-307">Console syntax</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="958c5-308">Este comando retorna uma matriz de objetos criados com o construtor especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-308">This command returns an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="958c5-309">O escopo de é o contexto de tempo de execução `queryObjects()` atualmente escolhido no **Console**.</span><span class="sxs-lookup"><span data-stu-id="958c5-309">The scope of `queryObjects()` is the currently chosen runtime context in the **Console**.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-310">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-310">Console example</span></span>  

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="958c5-311">Retorna todos `Promises` .</span><span class="sxs-lookup"><span data-stu-id="958c5-311">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="958c5-312">Retorna todos os elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="958c5-312">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="958c5-313">Retorna todos os objetos que foram instautados usando `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="958c5-313">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="958c5-314">tabela</span><span class="sxs-lookup"><span data-stu-id="958c5-314">table</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-315">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-315">Console syntax</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="958c5-316">Este comando registra dados de objeto com formatação de tabela com base no objeto de dados em com títulos opcionais de coluna.</span><span class="sxs-lookup"><span data-stu-id="958c5-316">This command logs object data with table formatting based upon the data object in with optional column headings.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-317">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-317">Console example</span></span>  

<span data-ttu-id="958c5-318">Na figura e exemplo de código a seguir, uma lista de nomes usando uma tabela no console é exibida.</span><span class="sxs-lookup"><span data-stu-id="958c5-318">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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
   <span data-ttu-id="958c5-320">O resultado do `table()` método</span><span class="sxs-lookup"><span data-stu-id="958c5-320">The result of the `table()` method</span></span>  
:::image-end:::  

---  

## <a name="undebug"></a><span data-ttu-id="958c5-321">undebug</span><span class="sxs-lookup"><span data-stu-id="958c5-321">undebug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-322">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-322">Console syntax</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="958c5-323">Este comando interrompe a depuração do método especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-323">This command stops the debug of the specified method.</span></span> <span data-ttu-id="958c5-324">Portanto, quando o método é solicitado, o depurador não é mais invocado.</span><span class="sxs-lookup"><span data-stu-id="958c5-324">So when the method is requested, the debugger is no longer invoked.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-325">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-325">Console example</span></span>  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a><span data-ttu-id="958c5-326">unmonitor</span><span class="sxs-lookup"><span data-stu-id="958c5-326">unmonitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-327">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-327">Console syntax</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="958c5-328">Este comando interrompe o monitoramento do método especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-328">This command stops the monitoring of the specified method.</span></span>  <span data-ttu-id="958c5-329">Esse método é usado em conjunto com o [método monitor().](#monitor)</span><span class="sxs-lookup"><span data-stu-id="958c5-329">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-330">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-330">Console example</span></span>  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a><span data-ttu-id="958c5-331">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="958c5-331">unmonitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-332">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-332">Console syntax</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="958c5-333">Este comando interrompe o monitoramento de eventos para o objeto e eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="958c5-333">This command stops monitoring events for the specified object and events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-334">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-334">Console example</span></span>  

<span data-ttu-id="958c5-335">Por exemplo, o trecho de código a seguir interrompe todo o monitoramento de eventos no objeto window.</span><span class="sxs-lookup"><span data-stu-id="958c5-335">For example, the following code snippet stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="958c5-336">Você também pode parar seletivamente o monitoramento de eventos específicos em um objeto.</span><span class="sxs-lookup"><span data-stu-id="958c5-336">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="958c5-337">Por exemplo, o código a seguir começa a monitorar todos os eventos no elemento escolhido no momento e interrompe o monitoramento de eventos \(talvez para reduzir o ruído na saída `mouse` `mousemove` do console\).</span><span class="sxs-lookup"><span data-stu-id="958c5-337">For example, the following code starts monitoring all `mouse` events on the currently chosen element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a><span data-ttu-id="958c5-338">values</span><span class="sxs-lookup"><span data-stu-id="958c5-338">values</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="958c5-339">Sintaxe do console</span><span class="sxs-lookup"><span data-stu-id="958c5-339">Console syntax</span></span>  

```console
values(object)
```  

<span data-ttu-id="958c5-340">Este comando retorna uma matriz que contém os valores de todas as propriedades pertencentes ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="958c5-340">This command returns an array containing the values of all properties belonging to the specified object.</span></span>  

### <a name="console-example"></a><span data-ttu-id="958c5-341">Exemplo de console</span><span class="sxs-lookup"><span data-stu-id="958c5-341">Console example</span></span>  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="958c5-342">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="958c5-342">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir - Referência da API de Console | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Como pausar seu código com pontos de interrupção Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Acelerar o tempo de execução do JavaScript | Microsoft Docs"  

[CR1050237]: https://crbug.com/1050237 "Problema 1050237: depuração(função) não está funcionando | Chromium bugs"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> <span data-ttu-id="958c5-352">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="958c5-352">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="958c5-353">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/utilities) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="958c5-353">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="958c5-355">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="958c5-355">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
