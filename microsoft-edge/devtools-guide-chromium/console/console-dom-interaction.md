---
description: Uma visão geral de como interagir com a página da Web atual no navegador usando a ferramenta Console
title: Usar o Console para interagir com o DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 80b0e4368b1c8feaf28a58ac2e3bd9c1ea2f1f92
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483292"
---
# <a name="use-the-console-to-interact-with-the-dom"></a><span data-ttu-id="8c367-104">Usar o Console para interagir com o DOM</span><span class="sxs-lookup"><span data-stu-id="8c367-104">Use the Console to interact with the DOM</span></span>

<span data-ttu-id="8c367-105">A **ferramenta Console** não é apenas para informações de registro em [log][DevtoolsConsoleConsoleLog] ou para [executar JavaScript arbitrário.][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="8c367-105">The **Console** tool isn't only for [logging information][DevtoolsConsoleConsoleLog] or to [run arbitrary JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  <span data-ttu-id="8c367-106">Também é uma ótima maneira de interagir com a página da Web no navegador.</span><span class="sxs-lookup"><span data-stu-id="8c367-106">It also is a great way to interact with the webpage in the browser.</span></span>  <span data-ttu-id="8c367-107">Considere-a uma versão de ambiente de script da **ferramenta Inspecionar.**</span><span class="sxs-lookup"><span data-stu-id="8c367-107">Consider it a script-environment version of the **Inspect** tool.</span></span>  

## <a name="read-from-the-dom"></a><span data-ttu-id="8c367-108">Leitura do DOM</span><span class="sxs-lookup"><span data-stu-id="8c367-108">Read from the DOM</span></span>

<span data-ttu-id="8c367-109">Para fazer referência ao header da página da Web, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8c367-109">To reference the header of the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c367-110">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-110">Open the **Console**.</span></span>
    *   <span data-ttu-id="8c367-111">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="8c367-111">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="8c367-112">Digite ou copie e copie o seguinte trecho de código no **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-112">Type or copy and paste the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Para fazer referência ao header no console, use document.querySelector" lightbox="../media/console-dom-get-reference.msft.png":::
    <span data-ttu-id="8c367-114">Para fazer referência ao header no console, use</span><span class="sxs-lookup"><span data-stu-id="8c367-114">To get a reference to the header in console, use</span></span> `document.querySelector`  
:::image-end:::  

<span data-ttu-id="8c367-115">Se você selecionar ou mover o cursor do mouse sobre o resultado `Shift` + `Tab` HTML, o DevTools realça o header para você.</span><span class="sxs-lookup"><span data-stu-id="8c367-115">If you select `Shift`+`Tab` or move your mouse cursor over the HTML result, DevTools highlights the header for you.</span></span>  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools realça a seção escolhida no Console" lightbox="../media/console-dom-highlight-element.msft.png":::
    <span data-ttu-id="8c367-117">DevTools realça a seção escolhida no **Console**</span><span class="sxs-lookup"><span data-stu-id="8c367-117">DevTools highlights the section you choose in the **Console**</span></span>  
:::image-end:::  

## <a name="manipulate-the-dom"></a><span data-ttu-id="8c367-118">Manipular o DOM</span><span class="sxs-lookup"><span data-stu-id="8c367-118">Manipulate the DOM</span></span>

<span data-ttu-id="8c367-119">Você também pode manipular a página da Web.</span><span class="sxs-lookup"><span data-stu-id="8c367-119">You may manipulate the webpage, too.</span></span>  <span data-ttu-id="8c367-120">Por exemplo, se você copiar e colar ou digitar o seguinte no **Console**, uma borda verde será exibida ao redor do header.</span><span class="sxs-lookup"><span data-stu-id="8c367-120">For example, if you copy and paste or type the following into the **Console**, a green border displays around the header.</span></span>

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Para adicionar uma borda a um elemento, use o Console" lightbox="../media/console-dom-add-border.msft.png":::
    <span data-ttu-id="8c367-122">Para adicionar uma borda a um elemento, use o **Console**</span><span class="sxs-lookup"><span data-stu-id="8c367-122">To add a border to an element, use the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-123">Dependendo da complexidade da página da Web, pode ser difícil encontrar o elemento certo para manipular.</span><span class="sxs-lookup"><span data-stu-id="8c367-123">Depending on the complexity of the webpage, It may be daunting to find the right element to manipulate.</span></span>  <span data-ttu-id="8c367-124">Mas você pode usar a **ferramenta Inspecionar** para ajudá-lo.</span><span class="sxs-lookup"><span data-stu-id="8c367-124">But you may use the **Inspect** tool to help you.</span></span>  <span data-ttu-id="8c367-125">Digamos que você queira manipular `Documentation` a parte no header.</span><span class="sxs-lookup"><span data-stu-id="8c367-125">Say you want to manipulate the `Documentation` part in the header.</span></span>

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Exibir o elemento que você inspecionar na tela" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    <span data-ttu-id="8c367-127">Exibir o elemento que você inspecionar na tela</span><span class="sxs-lookup"><span data-stu-id="8c367-127">Display the element that you inspect on the screen</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-128">Para obter uma referência direta ao elemento a ser manipulado, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8c367-128">To get a direct reference to the element to manipulate, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c367-129">Use a **ferramenta Inspecionar** para escolher o elemento.</span><span class="sxs-lookup"><span data-stu-id="8c367-129">Use the **Inspect** tool to choose the element.</span></span>  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Para escolher um elemento, use a ferramenta Inspector" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        <span data-ttu-id="8c367-131">Para escolher um elemento, use a **ferramenta Inspector**</span><span class="sxs-lookup"><span data-stu-id="8c367-131">To choose an element, use the **Inspector** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8c367-132">Escolha-o e o DevTools saltará para a **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="8c367-132">Choose it and DevTools jumps to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="8c367-133">Escolha o `...` menu ao lado do elemento no exibição DOM.</span><span class="sxs-lookup"><span data-stu-id="8c367-133">Choose the `...` menu next to the element in the DOM view.</span></span>  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="O elemento escolhido é exibido na árvore DOM da ferramenta Elementos, escolha o menu de estouro para obter mais recursos" lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        <span data-ttu-id="8c367-135">O elemento escolhido é exibido na árvore DOM da ferramenta **Elementos,** escolha o menu de estouro para obter mais recursos</span><span class="sxs-lookup"><span data-stu-id="8c367-135">The chosen element displays in the DOM tree of the **Elements** tool, choose the overflow menu to get more features</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8c367-136">Abra o menu contextual e escolha `Copy`  >  `Copy JS Path` .</span><span class="sxs-lookup"><span data-stu-id="8c367-136">Open the contextual menu and choose `Copy` > `Copy JS Path`.</span></span>  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Copie o caminho JavaScript de um elemento na exibição DOM da ferramenta Elements" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        <span data-ttu-id="8c367-138">Copie o caminho JavaScript de um elemento na exibição DOM da **ferramenta Elements**</span><span class="sxs-lookup"><span data-stu-id="8c367-138">Copy the JavaScript path from an element in the DOM view of the **Elements** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8c367-139">Volte para o **Console e** colar o comando.</span><span class="sxs-lookup"><span data-stu-id="8c367-139">Go back to the **Console** and paste the command.</span></span>  
    
<span data-ttu-id="8c367-140">Para alterar o texto do link para `My Playground` , adicione ao comando que você `.textContent = "My Playground"` colara anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8c367-140">To change the text of the link to `My Playground`, add `.textContent = "My Playground"` to the command you previously pasted.</span></span>  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Usar o Console para alterar o conteúdo de um elemento" lightbox="../media/console-dom-change-content.msft.png":::
    <span data-ttu-id="8c367-142">Usar o **Console** para alterar o conteúdo de um elemento</span><span class="sxs-lookup"><span data-stu-id="8c367-142">Use the **Console** to change the content of an element</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-143">Use quaisquer manipulações de DOM JavaScript que você deseja fazer no **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-143">Use any JavaScript DOM manipulations you want to do in the **Console**.</span></span>  <span data-ttu-id="8c367-144">Para torná-lo mais conveniente, o **Console** vem com alguns métodos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="8c367-144">To make it more convenient, the **Console** comes with a few helper methods.</span></span>  

## <a name="helpful-console-utility-methods"></a><span data-ttu-id="8c367-145">Métodos úteis de utilitário de Console</span><span class="sxs-lookup"><span data-stu-id="8c367-145">Helpful Console utility methods</span></span>  

<span data-ttu-id="8c367-146">Muitos métodos e atalhos de conveniência estão disponíveis para você como [Utilitários de Console.][DevtoolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="8c367-146">Many convenience methods and shortcuts are available to you as [Console Utilities][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="8c367-147">Alguns dos métodos são extremamente poderosos e são coisas que você provavelmente escreveu como uma série de `console.log()` instruções no passado.</span><span class="sxs-lookup"><span data-stu-id="8c367-147">Some of the methods are incredibly powerful and are things you probably wrote as a series of `console.log()` statements in the past.</span></span>

### <a name="the-power-to-the-"></a><span data-ttu-id="8c367-148">A potência para $</span><span class="sxs-lookup"><span data-stu-id="8c367-148">The power to the $</span></span>

<span data-ttu-id="8c367-149">O `$` tem potências especiais **no Console** e você pode se lembrar disso do jQuery.</span><span class="sxs-lookup"><span data-stu-id="8c367-149">The `$` has special powers in **Console** and you may remember that from jQuery.</span></span>

*   `$_` <span data-ttu-id="8c367-150">armazena o resultado do último comando.</span><span class="sxs-lookup"><span data-stu-id="8c367-150">stores the result of the last command.</span></span>  <span data-ttu-id="8c367-151">Portanto, se você digitar `2 + 2` e selecionar e digitar , o `Enter` `$_` **Console** exibirá você `4` .</span><span class="sxs-lookup"><span data-stu-id="8c367-151">So, if you type `2 + 2` and select `Enter`, and then type `$_`, the **Console** displays you `4`.</span></span>
*   `$0` <span data-ttu-id="8c367-152">to `$4` é uma pilha dos últimos elementos inspecionados é sempre o mais `$0` recente.</span><span class="sxs-lookup"><span data-stu-id="8c367-152">to `$4` is a stack of the last inspected elements `$0` is always the newest one.</span></span>  <span data-ttu-id="8c367-153">Portanto, no exemplo anterior, você acabou de escolher o elemento na ferramenta **Inspector** e digite `$0.textContent = "My Playground"` para obter o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="8c367-153">So in the earlier example, you just chose the element in the **Inspector** tool and type `$0.textContent = "My Playground"` to get the same effect.</span></span>
*   `$x()` <span data-ttu-id="8c367-154">permite que você escolha elementos DOM usando XPATH.</span><span class="sxs-lookup"><span data-stu-id="8c367-154">allows you to choose DOM elements using XPATH.</span></span>
*   `$()` <span data-ttu-id="8c367-155">e `$$()` são versões mais curtas de para `document.querySelector()` e `document.querySelectorAll()` .</span><span class="sxs-lookup"><span data-stu-id="8c367-155">and `$$()` are shorter versions of for `document.querySelector()` and `document.querySelectorAll()`.</span></span>  
    
<span data-ttu-id="8c367-156">Por exemplo, o trecho de código a seguir recupera todos os links na página da Web \(como é curto para \) e exibe os links como uma tabela sortível para copiar e colar, por exemplo, em `$$('a')` `document.querySelectorAll('a')` Excel.</span><span class="sxs-lookup"><span data-stu-id="8c367-156">For example, the following code snippet retrieves all the links in the webpage \(as `$$('a')` is short for `document.querySelectorAll('a')`\) and displays the links as a sortable table to copy and paste, for example, into Excel.</span></span>

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Obter todos os links na página da Web e exibir o resultado como uma tabela" lightbox="../media/console-dom-get-all-links.msft.png":::
    <span data-ttu-id="8c367-158">Obter todos os links na página da Web e exibir o resultado como uma tabela</span><span class="sxs-lookup"><span data-stu-id="8c367-158">Get all links in the webpage and display the result as a table</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-159">No entanto, se você não quiser exibir as informações, mas quiser agarrá-la como dados.</span><span class="sxs-lookup"><span data-stu-id="8c367-159">However, if you don't want to display the information, but you want to grab it as data.</span></span>  <span data-ttu-id="8c367-160">O `$$('a')` atalho fornece os links de âncora e todas as propriedades para cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="8c367-160">The `$$('a')` shortcut provides the anchor links and all of the properties for each one.</span></span>  <span data-ttu-id="8c367-161">O problema é que você só deseja os links e o texto relacionado.</span><span class="sxs-lookup"><span data-stu-id="8c367-161">The problem is that you only want the links and the related text.</span></span>  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="O atalho $$ retorna muitas informações" lightbox="../media/console-dom-too-much-link-information.msft.png":::
    <span data-ttu-id="8c367-163">O `$$` atalho retorna informações demais</span><span class="sxs-lookup"><span data-stu-id="8c367-163">The `$$` shortcut returns far too much information</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-164">O `$$` atalho tem um recurso extra interessante.</span><span class="sxs-lookup"><span data-stu-id="8c367-164">The `$$` shortcut has an interesting extra feature.</span></span>  <span data-ttu-id="8c367-165">Em vez de retornar uma forma `NodeList` pura como , o atalho fornece todos os `document.querySelectorAll()` `$$` `Array` métodos.</span><span class="sxs-lookup"><span data-stu-id="8c367-165">Instead of returning a pure `NodeList` like `document.querySelectorAll()`, the `$$` shortcut gives you all of the `Array` methods.</span></span>  <span data-ttu-id="8c367-166">Use `map()` o método para reduzir as informações ao que você precisa.</span><span class="sxs-lookup"><span data-stu-id="8c367-166">Use `map()` method to reduce the information to what you need.</span></span>  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

<span data-ttu-id="8c367-167">O trecho de código retorna uma Matriz de todos os links como objetos `url` com e `text` propriedades.</span><span class="sxs-lookup"><span data-stu-id="8c367-167">The code snippet returns an Array of all the links as objects with `url` and `text` properties.</span></span>  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Usar mapa em $$ para filtrar informações até o mínimo" lightbox="../media/console-dom-filter-link-data.msft.png":::
    <span data-ttu-id="8c367-169">Usar o mapa para `$$` filtrar informações até o mínimo</span><span class="sxs-lookup"><span data-stu-id="8c367-169">Use map on `$$` to filter information down to the bare minimum</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-170">Você ainda não terminou, vários links são links internos para a página da Web ou têm texto vazio.</span><span class="sxs-lookup"><span data-stu-id="8c367-170">You aren't done yet, several links are internal links to the webpage or have empty text.</span></span>  <span data-ttu-id="8c367-171">Use o método filter para se livrar dos links internos.</span><span class="sxs-lookup"><span data-stu-id="8c367-171">Use the filter method to get rid of the internal links.</span></span>  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Obter os links que não estão vazios e são externos" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    <span data-ttu-id="8c367-173">Obter os links que não estão vazios e são externos</span><span class="sxs-lookup"><span data-stu-id="8c367-173">Get the links that aren't empty and are external</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-174">Conforme exibido no início da página da Web, você também pode alterar esses elementos.</span><span class="sxs-lookup"><span data-stu-id="8c367-174">As displayed at the start of the webpage, you may also change these elements.</span></span>  <span data-ttu-id="8c367-175">Por exemplo, o trecho de código a seguir cria uma borda verde em torno de todos os links externos:</span><span class="sxs-lookup"><span data-stu-id="8c367-175">For example, the following code snippet creates a green border around all external links:</span></span>

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Para realçar todos os links externos, adicione uma borda verde ao redor de cada" lightbox="../media/console-dom-highlight-links.msft.png":::
    <span data-ttu-id="8c367-177">Para realçar todos os links externos, adicione uma borda verde ao redor de cada</span><span class="sxs-lookup"><span data-stu-id="8c367-177">To highlight all external links, add a green border around each</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-178">Em vez de escrever JavaScript complexo para filtrar resultados, use o poder dos seletores CSS.</span><span class="sxs-lookup"><span data-stu-id="8c367-178">Instead of writing complex JavaScript to filter results, use the power of CSS selectors.</span></span>  

<span data-ttu-id="8c367-179">Para criar uma tabela e informações para todas as imagens na página da Web que não são imagens em `src` `alt` linha, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8c367-179">To create a table of the `src` and `alt` information for all images on the webpage that aren't inline images, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c367-180">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="8c367-181">Digite ou copie e copie o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c367-181">Type or copy and paste the following code snippet.</span></span>  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Para escolher elementos, use um seletor CSS complexo" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    <span data-ttu-id="8c367-183">Para escolher elementos, use um seletor CSS complexo</span><span class="sxs-lookup"><span data-stu-id="8c367-183">To choose elements, use a complex CSS selector</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-184">Pronto para um exemplo ainda mais complexo?</span><span class="sxs-lookup"><span data-stu-id="8c367-184">Ready for an even more complex example?</span></span>  <span data-ttu-id="8c367-185">As páginas da Web HTML geradas a partir da marcação, como este artigo, têm valores de ID automáticos para cada título para permitir que você vincule profundamente essa seção.</span><span class="sxs-lookup"><span data-stu-id="8c367-185">HTML webpages generated from markdown like this article, have automatic ID values for each heading to allow you to deep link to that section.</span></span>  <span data-ttu-id="8c367-186">Por exemplo, uma `# New features` alteração para `<h1 id="new-features">New features</h1>` .</span><span class="sxs-lookup"><span data-stu-id="8c367-186">For example, a `# New features` changes to `<h1 id="new-features">New features</h1>`.</span></span>  

<span data-ttu-id="8c367-187">Para listar todos os títulos automáticos para copiar e colar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8c367-187">To list of all of the automatic headings to copy and paste, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c367-188">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-188">Open the **Console**.</span></span>  
1.  <span data-ttu-id="8c367-189">Digite ou copie e copie o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c367-189">Type or copy and paste the following code snippet.</span></span>  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

<span data-ttu-id="8c367-190">O resultado é o texto que contém conteúdo para cada título seguido pela URL completa que aponta para ele.</span><span class="sxs-lookup"><span data-stu-id="8c367-190">The result is text that contains content for each heading followed by the full URL that points to it.</span></span>  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Obter todos os títulos e AS URLs geradas na página da Web" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    <span data-ttu-id="8c367-192">Obter todos os títulos e AS URLs geradas na página da Web</span><span class="sxs-lookup"><span data-stu-id="8c367-192">Get all the headings and the generated URLs from the webpage</span></span>  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a><span data-ttu-id="8c367-193">Limpar com limpar e copiar</span><span class="sxs-lookup"><span data-stu-id="8c367-193">Clean up with clear and copy</span></span>

<span data-ttu-id="8c367-194">Ao desenvolver no **Console,** as coisas podem ficar confusas.</span><span class="sxs-lookup"><span data-stu-id="8c367-194">When developing in the **Console**, things may get messy.</span></span>  <span data-ttu-id="8c367-195">Você pode achar frustrante tentar escolher resultados enquanto copia e colar.</span><span class="sxs-lookup"><span data-stu-id="8c367-195">You may find it frustrating to try to choose results while you copy and paste.</span></span>  <span data-ttu-id="8c367-196">Os dois métodos utilitários a seguir ajudam você.</span><span class="sxs-lookup"><span data-stu-id="8c367-196">The following two utility methods help you.</span></span>  

*   `copy()` <span data-ttu-id="8c367-197">copia o que você der à área de transferência.</span><span class="sxs-lookup"><span data-stu-id="8c367-197">copies whatever you give it to the clipboard.</span></span>  <span data-ttu-id="8c367-198">O `copy()` método é especialmente útil quando você o mistura com o que copia o último `$_` resultado.</span><span class="sxs-lookup"><span data-stu-id="8c367-198">The `copy()` method is especially useful when you mix it with `$_` that copies the last result.</span></span>
*   `clear()` <span data-ttu-id="8c367-199">limpa o **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-199">clears the **Console**.</span></span>

### <a name="read-and-monitor-events"></a><span data-ttu-id="8c367-200">Ler e monitorar eventos</span><span class="sxs-lookup"><span data-stu-id="8c367-200">Read and monitor events</span></span>

<span data-ttu-id="8c367-201">Dois outros métodos utilitários interessantes de **Console** lidam com o tratamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="8c367-201">Two other interesting utility methods of **Console** deal with event handling.</span></span>

*   `getEventListeners(node)` <span data-ttu-id="8c367-202">lista todos os ouvintes de eventos de um nó.</span><span class="sxs-lookup"><span data-stu-id="8c367-202">lists all the event listeners of a node.</span></span>
*   `monitorEvents(node, events)` <span data-ttu-id="8c367-203">monitora e registra os eventos que ocorrem em um nó.</span><span class="sxs-lookup"><span data-stu-id="8c367-203">monitors and logs the events that happen on a node.</span></span>

<span data-ttu-id="8c367-204">Para listar todos os ouvintes de eventos atribuídos ao primeiro formulário na página da Web, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8c367-204">To list all of the event listener assigned to the first form in the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c367-205">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-205">Open the **Console**.</span></span>  
1.  <span data-ttu-id="8c367-206">Digite ou copie e copie o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c367-206">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Obter todos os ouvintes de eventos para o primeiro formulário na página da Web" lightbox="../media/console-dom-get-form-events.msft.png":::
    <span data-ttu-id="8c367-208">Obter todos os ouvintes de eventos para o primeiro formulário na página da Web</span><span class="sxs-lookup"><span data-stu-id="8c367-208">Get all events listeners for the first form in the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-209">Quando você monitora, você recebe uma notificação no **Console** sempre que algo muda para os elementos especificados.</span><span class="sxs-lookup"><span data-stu-id="8c367-209">When you monitor, you to get a notification in the **Console** every time something changes to the specified elements.</span></span>  <span data-ttu-id="8c367-210">Você define os eventos que deseja escutar como um segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8c367-210">You define the events you want to listen to as a second parameter.</span></span>  <span data-ttu-id="8c367-211">É importante que você defina os eventos que deseja monitorar, caso contrário, qualquer evento que aconteça com o elemento será relatado.</span><span class="sxs-lookup"><span data-stu-id="8c367-211">It is important for you to define the events that you want to monitor, otherwise any event happening to the element is reported.</span></span>

<span data-ttu-id="8c367-212">Para receber uma notificação no **Console** sempre que rolar, resize a janela ou quando o usuário digita no formulário de pesquisa, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8c367-212">To get a notification in the **Console** every time you scroll, resize the window, or when the user types in the search form, complete the following actions.</span></span>  

1.  <span data-ttu-id="8c367-213">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-213">Open the **Console**.</span></span>  
1.  <span data-ttu-id="8c367-214">Digite ou copie e copie o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c367-214">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="Console exibe cada evento de rolagem que acontece na Janela" lightbox="../media/console-dom-monitor-events.msft.png":::
    <span data-ttu-id="8c367-216">**Console** exibe cada evento de rolagem que acontece na Janela</span><span class="sxs-lookup"><span data-stu-id="8c367-216">**Console** displays every scroll event that happens on the Window</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-217">Para registrar qualquer ação de chave no elemento escolhido no momento, concentre-se no formulário de pesquisa no header e selecione algumas teclas.</span><span class="sxs-lookup"><span data-stu-id="8c367-217">To log any key action on the currently chosen element, focus on the search form in the header and select some keys.</span></span>  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="Console exibe eventos de keyup que ocorrem no formulário" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    <span data-ttu-id="8c367-219">**Console** exibe `keyup` eventos que ocorrem no formulário</span><span class="sxs-lookup"><span data-stu-id="8c367-219">**Console** displays `keyup` events that happen on the form</span></span>  
:::image-end:::  

<span data-ttu-id="8c367-220">Para impedi-lo, remova o monitoramento definido usando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c367-220">To stop it, remove the monitoring you set using the following code snippet.</span></span>  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a><span data-ttu-id="8c367-221">Reutilizar scripts de manipulação dom</span><span class="sxs-lookup"><span data-stu-id="8c367-221">Reuse DOM manipulation scripts</span></span>

<span data-ttu-id="8c367-222">Você pode achar útil manipular o DOM a partir do **Console**.</span><span class="sxs-lookup"><span data-stu-id="8c367-222">You may find it useful to manipulate the DOM from the **Console**.</span></span>  <span data-ttu-id="8c367-223">Em breve, você poderá executar as limitações do **Console** como uma plataforma de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="8c367-223">You may soon run into the limitations of the **Console** as a development platform.</span></span>  <span data-ttu-id="8c367-224">A boa notícia é que a [ferramenta Sources][DevtoolsSourcesIndex] no DevTools oferece um ambiente de desenvolvimento totalmente em destaque.</span><span class="sxs-lookup"><span data-stu-id="8c367-224">The good news is that the [Sources][DevtoolsSourcesIndex] tool in DevTools offers a fully featured development environment.</span></span>  <span data-ttu-id="8c367-225">Na ferramenta **Fontes,** você pode concluir as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8c367-225">In the **Sources** tool, you may complete the following actions.</span></span>  

*   <span data-ttu-id="8c367-226">Armazene seus scripts para **o Console** [como trechos de código.][DevToolsJavascriptSnippets]</span><span class="sxs-lookup"><span data-stu-id="8c367-226">Store your scripts for the **Console** as [Snippets][DevToolsJavascriptSnippets].</span></span>  
*   <span data-ttu-id="8c367-227">Execute os scripts em uma página da Web usando um atalho de teclado ou o editor.</span><span class="sxs-lookup"><span data-stu-id="8c367-227">Run the scripts in a webpage using a keyboard shortcut or the editor.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8c367-228">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8c367-228">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console como um ambiente JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Logs na ferramenta console | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página com Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSourcesIndex]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
