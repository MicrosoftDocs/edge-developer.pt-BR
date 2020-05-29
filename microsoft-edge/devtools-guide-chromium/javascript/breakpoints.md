---
title: Como pausar um código com pontos de interrupção no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 2afa4b7dbe96b65747ec17b147f0a82c16efa288
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581800"
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







# <span data-ttu-id="b587d-103">Como pausar um código com pontos de interrupção no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b587d-103">How To Pause Your Code With Breakpoints In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="b587d-104">Use pontos de interrupção para pausar o código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b587d-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="b587d-105">Este guia explica cada tipo de ponto de interrupção que está disponível no DevTools, bem como quando usar e como definir cada tipo.</span><span class="sxs-lookup"><span data-stu-id="b587d-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="b587d-106">Para um tutorial prático do processo de depuração, consulte [introdução à depuração de JavaScript no Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="b587d-106">For a hands-on tutorial of the debugging process, see [Get Started with Debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="b587d-107">Visão geral de quando usar cada tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="b587d-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="b587d-108">O tipo mais conhecido de ponto de interrupção é linha de código.</span><span class="sxs-lookup"><span data-stu-id="b587d-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="b587d-109">Mas os pontos de interrupção de linha de código podem ser ineficientemente definidos, especialmente se você não souber exatamente onde procurar ou se estiver trabalhando com uma grande codebase.</span><span class="sxs-lookup"><span data-stu-id="b587d-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="b587d-110">Você pode economizar tempo ao depurar sabendo como e quando usar os outros tipos de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b587d-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="b587d-111">Tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="b587d-111">Breakpoint Type</span></span> | <span data-ttu-id="b587d-112">Use isso quando desejar pausar...</span><span class="sxs-lookup"><span data-stu-id="b587d-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="b587d-113">Linha de código</span><span class="sxs-lookup"><span data-stu-id="b587d-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="b587d-114">Em uma região de código exata.</span><span class="sxs-lookup"><span data-stu-id="b587d-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="b587d-115">Linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="b587d-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="b587d-116">Em uma região de código exata, mas somente quando alguma outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="b587d-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="b587d-117">DOM</span><span class="sxs-lookup"><span data-stu-id="b587d-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="b587d-118">No código que altera ou remove um nó DOM específico ou os filhos.</span><span class="sxs-lookup"><span data-stu-id="b587d-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="b587d-119">XHR</span><span class="sxs-lookup"><span data-stu-id="b587d-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="b587d-120">Quando uma URL XHR contém um padrão de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b587d-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="b587d-121">Ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="b587d-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="b587d-122">No código que é executado após um evento, como `click` , é executado.</span><span class="sxs-lookup"><span data-stu-id="b587d-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="b587d-123">Extremamente</span><span class="sxs-lookup"><span data-stu-id="b587d-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="b587d-124">Na linha de código que está lançando uma exceção capturada ou não capturada.</span><span class="sxs-lookup"><span data-stu-id="b587d-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="b587d-125">Função</span><span class="sxs-lookup"><span data-stu-id="b587d-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="b587d-126">Sempre que um comando, função ou método específico é executado.</span><span class="sxs-lookup"><span data-stu-id="b587d-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="b587d-127">Pontos de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="b587d-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="b587d-128">Use um ponto de interrupção de linha de código quando souber a região exata de código que você precisa investigar.</span><span class="sxs-lookup"><span data-stu-id="b587d-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="b587d-129">O DevTools **sempre** pausa antes da execução desta linha de código.</span><span class="sxs-lookup"><span data-stu-id="b587d-129">DevTools **always** pauses before this line of code is run.</span></span>  

<span data-ttu-id="b587d-130">Para definir um ponto de interrupção de linha de código no DevTools:</span><span class="sxs-lookup"><span data-stu-id="b587d-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="b587d-131">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b587d-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b587d-132">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="b587d-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="b587d-133">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="b587d-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="b587d-134">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b587d-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="b587d-135">Clique nela.</span><span class="sxs-lookup"><span data-stu-id="b587d-135">Click on it.</span></span>  <span data-ttu-id="b587d-136">Um ícone vermelho é exibido ao lado da coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b587d-136">A red icon appears next to the line number column.</span></span>  

> ##### <span data-ttu-id="b587d-137">Figura 1</span><span class="sxs-lookup"><span data-stu-id="b587d-137">Figure 1</span></span>  
> <span data-ttu-id="b587d-138">Um ponto de interrupção de linha de código definido na linha 30</span><span class="sxs-lookup"><span data-stu-id="b587d-138">A line-of-code breakpoint set on line 30</span></span>  
> ![Um ponto de interrupção de linha do código][ImageLocBreakpoint]  

### <span data-ttu-id="b587d-140">Pontos de interrupção de linha de código no código</span><span class="sxs-lookup"><span data-stu-id="b587d-140">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="b587d-141">Execute o `debugger` método do seu código para pausar na linha.</span><span class="sxs-lookup"><span data-stu-id="b587d-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="b587d-142">Isso equivale a um [ponto de interrupção de linha de código](#line-of-code-breakpoints), exceto pelo fato de o ponto de interrupção ser definido no seu código, não na interface do usuário do devtools.</span><span class="sxs-lookup"><span data-stu-id="b587d-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="b587d-143">Pontos de interrupção de linha de código condicionais</span><span class="sxs-lookup"><span data-stu-id="b587d-143">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="b587d-144">Use um ponto de interrupção de linha de código condicional quando souber a região exata do código que você precisa investigar, mas deseja pausar somente quando outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="b587d-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="b587d-145">Para definir um ponto de interrupção de linha de código condicional:</span><span class="sxs-lookup"><span data-stu-id="b587d-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="b587d-146">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b587d-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b587d-147">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="b587d-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="b587d-148">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="b587d-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="b587d-149">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b587d-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="b587d-150">Clique com o botão direito do mouse no número da linha.</span><span class="sxs-lookup"><span data-stu-id="b587d-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="b587d-151">Selecione **Adicionar ponto de interrupção condicional**.</span><span class="sxs-lookup"><span data-stu-id="b587d-151">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="b587d-152">Uma caixa de diálogo é exibida abaixo da linha de código.</span><span class="sxs-lookup"><span data-stu-id="b587d-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="b587d-153">Insira sua condição na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b587d-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="b587d-154">Pressione `Enter` para ativar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b587d-154">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="b587d-155">Um ícone próximo à coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b587d-155">An icon next to the line number column.</span></span>  

> ##### <span data-ttu-id="b587d-156">Figura 2</span><span class="sxs-lookup"><span data-stu-id="b587d-156">Figure 2</span></span>  
> <span data-ttu-id="b587d-157">Um ponto de interrupção de linha de código condicional definido na linha 34</span><span class="sxs-lookup"><span data-stu-id="b587d-157">A conditional line-of-code breakpoint set on line 34</span></span>  
> ![Um ponto de interrupção de linha de código condicional][ImageConditionalLocBreakpoint]  

### <span data-ttu-id="b587d-159">Gerenciar pontos de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="b587d-159">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="b587d-160">Use o painel **pontos de interrupção** para desabilitar ou remover pontos de interrupção de linha de código de um único local.</span><span class="sxs-lookup"><span data-stu-id="b587d-160">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

> ##### <span data-ttu-id="b587d-161">Figura 3</span><span class="sxs-lookup"><span data-stu-id="b587d-161">Figure 3</span></span>  
> <span data-ttu-id="b587d-162">O painel **pontos de interrupção** mostrando dois pontos de interrupção de linha de código: um na linha `16` de `get-started.js` , outro na linha</span><span class="sxs-lookup"><span data-stu-id="b587d-162">The **Breakpoints** panel showing two line-of-code breakpoints: one on line `16` of `get-started.js`, another on line</span></span> `33`  
> ![O painel pontos de interrupção][ImageBreakpointsPanel]  

*   <span data-ttu-id="b587d-164">Marque a caixa de seleção ao lado de uma entrada para desabilitar esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b587d-164">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="b587d-165">Clique com o botão direito do mouse em uma entrada para remover esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b587d-165">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="b587d-166">Clique com o botão direito do mouse em qualquer lugar no painel **pontos de interrupção** para desativar todos os pontos de interrupção, desabilitar todos os pontos de interrupção ou remover todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b587d-166">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="b587d-167">Desabilitar todos os pontos de interrupção é equivalente a desmarcar cada um deles.</span><span class="sxs-lookup"><span data-stu-id="b587d-167">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="b587d-168">A desativação de todos os pontos de interrupção instrui o DevTools a ignorar todos os pontos de interrupção de linha de código, mas também manter o estado habilitado para que cada um esteja no mesmo estado de antes da reativação de cada um.</span><span class="sxs-lookup"><span data-stu-id="b587d-168">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  

> ##### <span data-ttu-id="b587d-169">Figura 4</span><span class="sxs-lookup"><span data-stu-id="b587d-169">Figure 4</span></span>  
> <span data-ttu-id="b587d-170">Pontos de interrupção desativados no painel **pontos de interrupção** são desativados e transparentes</span><span class="sxs-lookup"><span data-stu-id="b587d-170">Deactivated breakpoints in the **Breakpoints** pane are disabled and transparent</span></span>  
> ![Pontos de interrupção desativados no painel pontos de interrupção][ImageDeactivatedBreakpoints]  

## <span data-ttu-id="b587d-172">Alterar o DOM dos pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="b587d-172">DOM change breakpoints</span></span>   

<span data-ttu-id="b587d-173">Use um ponto de interrupção de alteração DOM quando desejar pausar no código que altera um nó DOM ou filhos.</span><span class="sxs-lookup"><span data-stu-id="b587d-173">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="b587d-174">Para definir um ponto de interrupção de alteração DOM:</span><span class="sxs-lookup"><span data-stu-id="b587d-174">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="b587d-175">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="b587d-175">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="b587d-176">Vá para o elemento no qual você deseja definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b587d-176">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="b587d-177">Clique com o botão direito do mouse no elemento.</span><span class="sxs-lookup"><span data-stu-id="b587d-177">Right-click the element.</span></span>  
1.  <span data-ttu-id="b587d-178">Passe o mouse sobre a **pausa**e, em seguida, selecione **modificações de subárvore**, **modificações de atributo**ou remoção de **nó**.</span><span class="sxs-lookup"><span data-stu-id="b587d-178">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  

> ##### <span data-ttu-id="b587d-179">Figura 5</span><span class="sxs-lookup"><span data-stu-id="b587d-179">Figure 5</span></span>  
> <span data-ttu-id="b587d-180">O menu de contexto para a criação de um ponto de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="b587d-180">The context menu for creating a DOM change breakpoint</span></span>  
> ![O menu de contexto para a criação de um ponto de interrupção de alteração DOM][ImageDomChangeBreakpoint]  

### <span data-ttu-id="b587d-182">Tipos de pontos de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="b587d-182">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="b587d-183">**Modificações em subárvores**.</span><span class="sxs-lookup"><span data-stu-id="b587d-183">**Subtree modifications**.</span></span>  <span data-ttu-id="b587d-184">Disparado quando um filho do nó selecionado no momento é removido ou adicionado, ou o conteúdo de um filho é alterado.</span><span class="sxs-lookup"><span data-stu-id="b587d-184">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="b587d-185">Não disparado em alterações de atributo de nó filho ou em qualquer alteração do nó atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="b587d-185">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  

*   <span data-ttu-id="b587d-186">**Modificações de atributos**: disparadas quando um atributo é adicionado ou removido no nó selecionado atualmente ou quando um valor de atributo é alterado.</span><span class="sxs-lookup"><span data-stu-id="b587d-186">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  

*   <span data-ttu-id="b587d-187">**Remoção de nó**: disparada quando o nó selecionado no momento é removido.</span><span class="sxs-lookup"><span data-stu-id="b587d-187">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  

## <span data-ttu-id="b587d-188">Pontos de interrupção XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="b587d-188">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="b587d-189">Use um ponto de interrupção XHR quando você quiser interromper quando a URL de solicitação de um XHR contiver uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="b587d-189">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="b587d-190">DevTools pausa na linha de código em que XHR executa o `send()` método.</span><span class="sxs-lookup"><span data-stu-id="b587d-190">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="b587d-191">Esse recurso também funciona com solicitações de [busca de API][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="b587d-191">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="b587d-192">Um exemplo de quando isso é útil é quando você vê que sua página está solicitando uma URL incorreta, e você deseja localizar rapidamente o código-fonte do AJAX ou de busca que está causando a solicitação incorreta.</span><span class="sxs-lookup"><span data-stu-id="b587d-192">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="b587d-193">Para definir um ponto de interrupção XHR:</span><span class="sxs-lookup"><span data-stu-id="b587d-193">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="b587d-194">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b587d-194">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b587d-195">Expanda o painel **pontos de interrupção XHR** .</span><span class="sxs-lookup"><span data-stu-id="b587d-195">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="b587d-196">Clique em **Adicionar ponto de interrupção**.</span><span class="sxs-lookup"><span data-stu-id="b587d-196">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="b587d-197">Digite a cadeia de caracteres na qual você deseja interromper.</span><span class="sxs-lookup"><span data-stu-id="b587d-197">Enter the string which you want to break on.</span></span>  <span data-ttu-id="b587d-198">DevTools pausa quando essa cadeia de caracteres está presente em qualquer lugar em uma URL de solicitação XHR.</span><span class="sxs-lookup"><span data-stu-id="b587d-198">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="b587d-199">Pressione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="b587d-199">Press `Enter` to confirm.</span></span>  

> ##### <span data-ttu-id="b587d-200">Figura 6</span><span class="sxs-lookup"><span data-stu-id="b587d-200">Figure 6</span></span>  
> <span data-ttu-id="b587d-201">Criando um ponto de interrupção XHR nos **pontos de interrupção XHR** para qualquer solicitação que contém `org` na URL</span><span class="sxs-lookup"><span data-stu-id="b587d-201">Creating an XHR breakpoint in the **XHR Breakpoints** for any request that contains `org` in the URL</span></span>  
> ![Criando um ponto de interrupção XHR][ImageXhrBreakpoint]  

## <span data-ttu-id="b587d-203">Pontos de interrupção do ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="b587d-203">Event listener breakpoints</span></span> 

<span data-ttu-id="b587d-204">Use pontos de interrupção de ouvinte de eventos quando desejar pausar no código de ouvinte de eventos que é executado após a disparação de um evento.</span><span class="sxs-lookup"><span data-stu-id="b587d-204">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="b587d-205">Você pode selecionar eventos específicos, como `click` , ou categorias de eventos, como todos os eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="b587d-205">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="b587d-206">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b587d-206">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b587d-207">Expanda o painel **pontos de interrupção de ouvinte de eventos** .</span><span class="sxs-lookup"><span data-stu-id="b587d-207">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="b587d-208">DevTools mostra uma lista de categorias de eventos, como **animação**.</span><span class="sxs-lookup"><span data-stu-id="b587d-208">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="b587d-209">Verifique uma dessas categorias para pausar sempre que qualquer evento dessa categoria for acionado ou expandir a categoria e verificar um evento específico.</span><span class="sxs-lookup"><span data-stu-id="b587d-209">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  

> ##### <span data-ttu-id="b587d-210">Figura 7</span><span class="sxs-lookup"><span data-stu-id="b587d-210">Figure 7</span></span>  
> <span data-ttu-id="b587d-211">Criando um ponto de interrupção de ouvinte de eventos para</span><span class="sxs-lookup"><span data-stu-id="b587d-211">Creating an event listener breakpoint for</span></span> `deviceorientation`  
> ![Criando um ponto de interrupção de ouvinte de eventos][ImageEventListenerBreakpoint]  

## <span data-ttu-id="b587d-213">Pontos de interrupção de exceção</span><span class="sxs-lookup"><span data-stu-id="b587d-213">Exception breakpoints</span></span>   

<span data-ttu-id="b587d-214">Use pontos de interrupção de exceção quando desejar pausar na linha de código que está lançando uma exceção capturada ou não percebida.</span><span class="sxs-lookup"><span data-stu-id="b587d-214">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="b587d-215">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b587d-215">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b587d-216">Clique em **Pausar nas exceções** ![ pausa nas exceções ][ImagePauseOnExceptionsIcon] .</span><span class="sxs-lookup"><span data-stu-id="b587d-216">Click **Pause on exceptions** ![Pause on exceptions][ImagePauseOnExceptionsIcon].</span></span>  <span data-ttu-id="b587d-217">O ícone fica azul quando habilitado.</span><span class="sxs-lookup"><span data-stu-id="b587d-217">The icon turns blue when enabled.</span></span>  
    
    > ##### <span data-ttu-id="b587d-218">Figura 8</span><span class="sxs-lookup"><span data-stu-id="b587d-218">Figure 8</span></span>  
    > <span data-ttu-id="b587d-219">O botão **Pausar exceções**</span><span class="sxs-lookup"><span data-stu-id="b587d-219">The **Pause on exceptions** button</span></span>  
    > ![O botão Pausar exceções][ImagePauseExceptionsHighlight]  

1.  <span data-ttu-id="b587d-221">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="b587d-221">**Optional**.</span></span> <span data-ttu-id="b587d-222">Marque a caixa de seleção **Pausar exceções capturadas** se você também quiser pausar em exceções capturadas, além de não capturadas.</span><span class="sxs-lookup"><span data-stu-id="b587d-222">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  

> ##### <span data-ttu-id="b587d-223">Figura 9</span><span class="sxs-lookup"><span data-stu-id="b587d-223">Figure 9</span></span>  
> <span data-ttu-id="b587d-224">Pausado em uma exceção não capturada</span><span class="sxs-lookup"><span data-stu-id="b587d-224">Paused on an uncaught exception</span></span>  
> ![Pausado em uma exceção não capturada][ImageUncaughtException]  

## <span data-ttu-id="b587d-226">Pontos de interrupção de função</span><span class="sxs-lookup"><span data-stu-id="b587d-226">Function breakpoints</span></span>   

<span data-ttu-id="b587d-227">Execute o `debug(method)` método, onde `method` é o comando, a função ou o método que você deseja depurar, quando desejar pausar sempre que uma função específica for executada.</span><span class="sxs-lookup"><span data-stu-id="b587d-227">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="b587d-228">Você pode inserir `debug()` no seu código (como uma `console.log()` instrução) ou executar o método no console do devtools.</span><span class="sxs-lookup"><span data-stu-id="b587d-228">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="b587d-229">equivale a definir um [ponto de interrupção de linha do código](#line-of-code-breakpoints) na primeira linha da função.</span><span class="sxs-lookup"><span data-stu-id="b587d-229">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="b587d-230">Verifique se a função de destino está em escopo</span><span class="sxs-lookup"><span data-stu-id="b587d-230">Make sure the target function is in scope</span></span>   

<span data-ttu-id="b587d-231">DevTools lança uma `ReferenceError` se a função que você deseja depurar não está em escopo.</span><span class="sxs-lookup"><span data-stu-id="b587d-231">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

<span data-ttu-id="b587d-232">Garantir que a função de destino está em escopo é difícil se você estiver executando o `debug()` método do console devtools.</span><span class="sxs-lookup"><span data-stu-id="b587d-232">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="b587d-233">Aqui está uma estratégia:</span><span class="sxs-lookup"><span data-stu-id="b587d-233">Here is one strategy:</span></span>  

1.  <span data-ttu-id="b587d-234">Defina um [ponto de interrupção de linha do código](#line-of-code-breakpoints) em um local onde a função esteja no escopo.</span><span class="sxs-lookup"><span data-stu-id="b587d-234">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="b587d-235">Disparar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b587d-235">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="b587d-236">Execute o `debug()` método no console devtools enquanto o código ainda está pausado no ponto de interrupção da linha de código.</span><span class="sxs-lookup"><span data-stu-id="b587d-236">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  

 



<!-- image links -->  

[ImagePauseOnExceptionsIcon]: /microsoft-edge/devtools-guide-chromium/media/pause-on-exceptions-icon.msft.png  

[ImageLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoint-30.msft.png "Figura 1: um ponto de interrupção de linha de código"  
[ImageConditionalLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-conditional-breakpoint.msft.png "Figura 2: um ponto de interrupção de linha de código condicional"  
[ImageBreakpointsPanel]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-16-33.msft.png "Figura 3: o painel pontos de interrupção"  
[ImageDeactivatedBreakpoints]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png "Figura 4: pontos de interrupção desativados no painel pontos de interrupção"  
[ImageDomChangeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-elements-break-on-subtree-modifications.msft.png "Figura 5: o menu de contexto para a criação de um ponto de interrupção de alteração DOM"  
[ImageXhrBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png "Figura 6: Criando um ponto de interrupção XHR"  
[ImageEventListenerBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png "Figura 7: Criando um ponto de interrupção de ouvinte de eventos"  
[ImagePauseExceptionsHighlight]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-pause-on-exceptions.msft.png "Figura 8: o botão Pausar exceções"  
[ImageUncaughtException]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-paused-on-exception.msft.png "Figura 9: pausado em uma exceção não capturada"  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar API | MDN"  

> [!NOTE]
> <span data-ttu-id="b587d-248">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="b587d-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b587d-249">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b587d-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b587d-251">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b587d-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
