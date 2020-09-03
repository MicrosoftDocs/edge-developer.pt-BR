---
description: Saiba mais sobre as maneiras como você pode pausar seu código no Microsoft Edge DevTools.
title: Como pausar um código com pontos de interrupção no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 95aba99c2cfe87f26704faa20964ace5d2abdf51
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992803"
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







# <span data-ttu-id="12929-104">Como pausar um código com pontos de interrupção no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="12929-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="12929-105">Use pontos de interrupção para pausar o código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12929-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="12929-106">Este guia explica cada tipo de ponto de interrupção que está disponível no DevTools, bem como quando usar e como definir cada tipo.</span><span class="sxs-lookup"><span data-stu-id="12929-106">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="12929-107">Para um tutorial prático do processo de depuração, consulte [introdução à depuração de JavaScript no Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="12929-107">For a hands-on tutorial of the debugging process, see [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="12929-108">Visão geral de quando usar cada tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="12929-108">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="12929-109">O tipo mais conhecido de ponto de interrupção é linha de código.</span><span class="sxs-lookup"><span data-stu-id="12929-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="12929-110">Mas os pontos de interrupção de linha de código podem ser ineficientemente definidos, especialmente se você não souber exatamente onde procurar ou se estiver trabalhando com uma grande codebase.</span><span class="sxs-lookup"><span data-stu-id="12929-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="12929-111">Você pode economizar tempo ao depurar sabendo como e quando usar os outros tipos de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="12929-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="12929-112">Tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="12929-112">Breakpoint Type</span></span> | <span data-ttu-id="12929-113">Use isso quando desejar pausar...</span><span class="sxs-lookup"><span data-stu-id="12929-113">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="12929-114">Linha de código</span><span class="sxs-lookup"><span data-stu-id="12929-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="12929-115">Em uma região de código exata.</span><span class="sxs-lookup"><span data-stu-id="12929-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="12929-116">Linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="12929-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="12929-117">Em uma região de código exata, mas somente quando alguma outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="12929-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="12929-118">DOM</span><span class="sxs-lookup"><span data-stu-id="12929-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="12929-119">No código que altera ou remove um nó DOM específico ou os filhos.</span><span class="sxs-lookup"><span data-stu-id="12929-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="12929-120">XHR</span><span class="sxs-lookup"><span data-stu-id="12929-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="12929-121">Quando uma URL XHR contém um padrão de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="12929-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="12929-122">Ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="12929-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="12929-123">No código que é executado após um evento, como `click` , é executado.</span><span class="sxs-lookup"><span data-stu-id="12929-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="12929-124">Extremamente</span><span class="sxs-lookup"><span data-stu-id="12929-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="12929-125">Na linha de código que está lançando uma exceção capturada ou não capturada.</span><span class="sxs-lookup"><span data-stu-id="12929-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="12929-126">Função</span><span class="sxs-lookup"><span data-stu-id="12929-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="12929-127">Sempre que um comando, função ou método específico é executado.</span><span class="sxs-lookup"><span data-stu-id="12929-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="12929-128">Pontos de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="12929-128">Line-of-code breakpoints</span></span>   

<span data-ttu-id="12929-129">Use um ponto de interrupção de linha de código quando souber a região exata de código que você precisa investigar.</span><span class="sxs-lookup"><span data-stu-id="12929-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="12929-130">O DevTools sempre pausa antes da execução desta linha de código.</span><span class="sxs-lookup"><span data-stu-id="12929-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="12929-131">Para definir um ponto de interrupção de linha de código no DevTools:</span><span class="sxs-lookup"><span data-stu-id="12929-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="12929-132">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="12929-132">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="12929-133">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="12929-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="12929-134">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="12929-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="12929-135">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="12929-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="12929-136">Clique nela.</span><span class="sxs-lookup"><span data-stu-id="12929-136">Click on it.</span></span>  <span data-ttu-id="12929-137">Um ícone vermelho é exibido ao lado da coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="12929-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="12929-139">Um ponto de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="12929-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="12929-140">Pontos de interrupção de linha de código no código</span><span class="sxs-lookup"><span data-stu-id="12929-140">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="12929-141">Execute o `debugger` método do seu código para pausar na linha.</span><span class="sxs-lookup"><span data-stu-id="12929-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="12929-142">Isso equivale a um [ponto de interrupção de linha de código](#line-of-code-breakpoints), exceto pelo fato de o ponto de interrupção ser definido no seu código, não na interface do usuário do devtools.</span><span class="sxs-lookup"><span data-stu-id="12929-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="12929-143">Pontos de interrupção de linha de código condicionais</span><span class="sxs-lookup"><span data-stu-id="12929-143">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="12929-144">Use um ponto de interrupção de linha de código condicional quando souber a região exata do código que você precisa investigar, mas deseja pausar somente quando outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="12929-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="12929-145">Para definir um ponto de interrupção de linha de código condicional:</span><span class="sxs-lookup"><span data-stu-id="12929-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="12929-146">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="12929-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="12929-147">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="12929-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="12929-148">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="12929-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="12929-149">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="12929-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="12929-150">Clique com o botão direito do mouse no número da linha.</span><span class="sxs-lookup"><span data-stu-id="12929-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="12929-151">Selecione **Adicionar ponto de interrupção condicional**.</span><span class="sxs-lookup"><span data-stu-id="12929-151">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="12929-152">Uma caixa de diálogo é exibida abaixo da linha de código.</span><span class="sxs-lookup"><span data-stu-id="12929-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="12929-153">Insira sua condição na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="12929-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="12929-154">Pressione `Enter` para ativar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="12929-154">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="12929-155">Um ícone próximo à coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="12929-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Um ponto de interrupção de linha de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="12929-157">Um ponto de interrupção de linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="12929-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="12929-158">Gerenciar pontos de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="12929-158">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="12929-159">Use o painel **pontos de interrupção** para desabilitar ou remover pontos de interrupção de linha de código de um único local.</span><span class="sxs-lookup"><span data-stu-id="12929-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="O painel pontos de interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="12929-161">O painel **pontos de interrupção**</span><span class="sxs-lookup"><span data-stu-id="12929-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="12929-162">Marque a caixa de seleção ao lado de uma entrada para desabilitar esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="12929-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="12929-163">Clique com o botão direito do mouse em uma entrada para remover esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="12929-163">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="12929-164">Clique com o botão direito do mouse em qualquer lugar no painel **pontos de interrupção** para desativar todos os pontos de interrupção, desabilitar todos os pontos de interrupção ou remover todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="12929-164">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="12929-165">Desabilitar todos os pontos de interrupção é equivalente a desmarcar cada um deles.</span><span class="sxs-lookup"><span data-stu-id="12929-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="12929-166">A desativação de todos os pontos de interrupção instrui o DevTools a ignorar todos os pontos de interrupção de linha de código, mas também manter o estado habilitado para que cada um esteja no mesmo estado de antes da reativação de cada um.</span><span class="sxs-lookup"><span data-stu-id="12929-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Pontos de interrupção desativados no painel pontos de interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="12929-168">Pontos de interrupção desativados no painel **pontos de interrupção**</span><span class="sxs-lookup"><span data-stu-id="12929-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="12929-169">Alterar o DOM dos pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="12929-169">DOM change breakpoints</span></span>   

<span data-ttu-id="12929-170">Use um ponto de interrupção de alteração DOM quando desejar pausar no código que altera um nó DOM ou filhos.</span><span class="sxs-lookup"><span data-stu-id="12929-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="12929-171">Para definir um ponto de interrupção de alteração DOM:</span><span class="sxs-lookup"><span data-stu-id="12929-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="12929-172">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="12929-172">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="12929-173">Vá para o elemento no qual você deseja definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="12929-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="12929-174">Clique com o botão direito do mouse no elemento.</span><span class="sxs-lookup"><span data-stu-id="12929-174">Right-click the element.</span></span>  
1.  <span data-ttu-id="12929-175">Passe o mouse sobre a **pausa**e, em seguida, selecione **modificações de subárvore**, **modificações de atributo**ou remoção de **nó**.</span><span class="sxs-lookup"><span data-stu-id="12929-175">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="O menu de contexto para a criação de um ponto de interrupção de alteração DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="12929-177">O menu de contexto para a criação de um ponto de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="12929-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="12929-178">Tipos de pontos de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="12929-178">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="12929-179">**Modificações em subárvores**.</span><span class="sxs-lookup"><span data-stu-id="12929-179">**Subtree modifications**.</span></span>  <span data-ttu-id="12929-180">Disparado quando um filho do nó selecionado no momento é removido ou adicionado, ou o conteúdo de um filho é alterado.</span><span class="sxs-lookup"><span data-stu-id="12929-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="12929-181">Não disparado em alterações de atributo de nó filho ou em qualquer alteração do nó atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="12929-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="12929-182">**Modificações de atributos**: disparadas quando um atributo é adicionado ou removido no nó selecionado atualmente ou quando um valor de atributo é alterado.</span><span class="sxs-lookup"><span data-stu-id="12929-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="12929-183">**Remoção de nó**: disparada quando o nó selecionado no momento é removido.</span><span class="sxs-lookup"><span data-stu-id="12929-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="12929-184">Pontos de interrupção XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="12929-184">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="12929-185">Use um ponto de interrupção XHR quando você quiser interromper quando a URL de solicitação de um XHR contiver uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="12929-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="12929-186">DevTools pausa na linha de código em que XHR executa o `send()` método.</span><span class="sxs-lookup"><span data-stu-id="12929-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="12929-187">Esse recurso também funciona com solicitações de [busca de API][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="12929-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="12929-188">Um exemplo de quando isso é útil é quando você vê que sua página está solicitando uma URL incorreta, e você deseja localizar rapidamente o código-fonte do AJAX ou de busca que está causando a solicitação incorreta.</span><span class="sxs-lookup"><span data-stu-id="12929-188">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="12929-189">Para definir um ponto de interrupção XHR:</span><span class="sxs-lookup"><span data-stu-id="12929-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="12929-190">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="12929-190">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="12929-191">Expanda o painel **pontos de interrupção XHR** .</span><span class="sxs-lookup"><span data-stu-id="12929-191">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="12929-192">Clique em **Adicionar ponto de interrupção**.</span><span class="sxs-lookup"><span data-stu-id="12929-192">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="12929-193">Digite a cadeia de caracteres na qual você deseja interromper.</span><span class="sxs-lookup"><span data-stu-id="12929-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="12929-194">DevTools pausa quando essa cadeia de caracteres está presente em qualquer lugar em uma URL de solicitação XHR.</span><span class="sxs-lookup"><span data-stu-id="12929-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="12929-195">Pressione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="12929-195">Press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Criar um ponto de interrupção XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="12929-197">Criar um ponto de interrupção XHR</span><span class="sxs-lookup"><span data-stu-id="12929-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="12929-198">Pontos de interrupção do ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="12929-198">Event listener breakpoints</span></span> 

<span data-ttu-id="12929-199">Use pontos de interrupção de ouvinte de eventos quando desejar pausar no código de ouvinte de eventos que é executado após a disparação de um evento.</span><span class="sxs-lookup"><span data-stu-id="12929-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="12929-200">Você pode selecionar eventos específicos, como `click` , ou categorias de eventos, como todos os eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="12929-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="12929-201">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="12929-201">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="12929-202">Expanda o painel **pontos de interrupção de ouvinte de eventos** .</span><span class="sxs-lookup"><span data-stu-id="12929-202">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="12929-203">DevTools mostra uma lista de categorias de eventos, como **animação**.</span><span class="sxs-lookup"><span data-stu-id="12929-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="12929-204">Verifique uma dessas categorias para pausar sempre que qualquer evento dessa categoria for acionado ou expandir a categoria e verificar um evento específico.</span><span class="sxs-lookup"><span data-stu-id="12929-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Criar um ponto de interrupção de ouvinte de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="12929-206">Criar um ponto de interrupção de ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="12929-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="12929-207">Pontos de interrupção de exceção</span><span class="sxs-lookup"><span data-stu-id="12929-207">Exception breakpoints</span></span>   

<span data-ttu-id="12929-208">Use pontos de interrupção de exceção quando desejar pausar na linha de código que está lançando uma exceção capturada ou não percebida.</span><span class="sxs-lookup"><span data-stu-id="12929-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="12929-209">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="12929-209">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="12929-210">Clique em **Pausar nas exceções** \ ( ![ Pausar exceções ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="12929-210">Click **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="12929-211">O ícone fica azul quando habilitado.</span><span class="sxs-lookup"><span data-stu-id="12929-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="O botão Pausar exceções" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="12929-213">O botão **Pausar exceções**</span><span class="sxs-lookup"><span data-stu-id="12929-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="12929-214">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="12929-214">**Optional**.</span></span>  <span data-ttu-id="12929-215">Marque a caixa de seleção **Pausar exceções capturadas** se você também quiser pausar em exceções capturadas, além de não capturadas.</span><span class="sxs-lookup"><span data-stu-id="12929-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausado em uma exceção não capturada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="12929-217">Pausado em uma exceção não capturada</span><span class="sxs-lookup"><span data-stu-id="12929-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="12929-218">Pontos de interrupção de função</span><span class="sxs-lookup"><span data-stu-id="12929-218">Function breakpoints</span></span>   

<span data-ttu-id="12929-219">Execute o `debug(method)` método, onde `method` é o comando, a função ou o método que você deseja depurar, quando desejar pausar sempre que uma função específica for executada.</span><span class="sxs-lookup"><span data-stu-id="12929-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="12929-220">Você pode inserir `debug()` no seu código (como uma `console.log()` instrução) ou executar o método no console do devtools.</span><span class="sxs-lookup"><span data-stu-id="12929-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="12929-221">equivale a definir um [ponto de interrupção de linha do código](#line-of-code-breakpoints) na primeira linha da função.</span><span class="sxs-lookup"><span data-stu-id="12929-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="12929-222">Verifique se a função de destino está em escopo</span><span class="sxs-lookup"><span data-stu-id="12929-222">Make sure the target function is in scope</span></span>   

<span data-ttu-id="12929-223">DevTools lança uma `ReferenceError` se a função que você deseja depurar não está em escopo.</span><span class="sxs-lookup"><span data-stu-id="12929-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="12929-224">Garantir que a função de destino está em escopo é difícil se você estiver executando o `debug()` método do console devtools.</span><span class="sxs-lookup"><span data-stu-id="12929-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="12929-225">Aqui está uma estratégia:</span><span class="sxs-lookup"><span data-stu-id="12929-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="12929-226">Defina um [ponto de interrupção de linha do código](#line-of-code-breakpoints) em um local onde a função esteja no escopo.</span><span class="sxs-lookup"><span data-stu-id="12929-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="12929-227">Disparar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="12929-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="12929-228">Execute o `debug()` método no console devtools enquanto o código ainda está pausado no ponto de interrupção da linha de código.</span><span class="sxs-lookup"><span data-stu-id="12929-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introdução à depuração JavaScript no Microsoft Edge DevTools | Documentos da Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar API | MDN"  

> [!NOTE]
> <span data-ttu-id="12929-231">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="12929-231">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="12929-232">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="12929-232">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="12929-234">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="12929-234">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
