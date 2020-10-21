---
description: Saiba mais sobre as maneiras como você pode pausar seu código no Microsoft Edge DevTools.
title: Como pausar um código com pontos de interrupção no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 98c0e42657d9b0900d3eaca8af69f1c17abfcf06
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124807"
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

# <span data-ttu-id="b8deb-104">Como pausar um código com pontos de interrupção no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b8deb-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b8deb-105">Use pontos de interrupção para pausar o código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b8deb-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="b8deb-106">Este guia explica cada tipo de ponto de interrupção que está disponível no DevTools, bem como quando usar e como definir cada tipo.</span><span class="sxs-lookup"><span data-stu-id="b8deb-106">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="b8deb-107">Para obter um tutorial prático do processo de depuração, navegue até [introdução ao Debugging JavaScript in Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="b8deb-107">For a hands-on tutorial of the debugging process, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="b8deb-108">Visão geral de quando usar cada tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="b8deb-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="b8deb-109">O tipo mais conhecido de ponto de interrupção é linha de código.</span><span class="sxs-lookup"><span data-stu-id="b8deb-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="b8deb-110">Mas os pontos de interrupção de linha de código podem ser ineficientemente definidos, especialmente se você não souber exatamente onde procurar ou se estiver trabalhando com uma grande codebase.</span><span class="sxs-lookup"><span data-stu-id="b8deb-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="b8deb-111">Você pode economizar tempo ao depurar sabendo como e quando usar os outros tipos de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b8deb-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="b8deb-112">Tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="b8deb-112">Breakpoint Type</span></span> | <span data-ttu-id="b8deb-113">Use isso quando desejar pausar...</span><span class="sxs-lookup"><span data-stu-id="b8deb-113">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="b8deb-114">Linha de código</span><span class="sxs-lookup"><span data-stu-id="b8deb-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="b8deb-115">Em uma região de código exata.</span><span class="sxs-lookup"><span data-stu-id="b8deb-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="b8deb-116">Linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="b8deb-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="b8deb-117">Em uma região de código exata, mas somente quando alguma outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="b8deb-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="b8deb-118">DOM</span><span class="sxs-lookup"><span data-stu-id="b8deb-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="b8deb-119">No código que altera ou remove um nó DOM específico ou os filhos.</span><span class="sxs-lookup"><span data-stu-id="b8deb-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="b8deb-120">XHR</span><span class="sxs-lookup"><span data-stu-id="b8deb-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="b8deb-121">Quando uma URL XHR contém um padrão de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b8deb-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="b8deb-122">Ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="b8deb-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="b8deb-123">No código que é executado após um evento, como `click` , é executado.</span><span class="sxs-lookup"><span data-stu-id="b8deb-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="b8deb-124">Extremamente</span><span class="sxs-lookup"><span data-stu-id="b8deb-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="b8deb-125">Na linha de código que está lançando uma exceção capturada ou não capturada.</span><span class="sxs-lookup"><span data-stu-id="b8deb-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="b8deb-126">Função</span><span class="sxs-lookup"><span data-stu-id="b8deb-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="b8deb-127">Sempre que um comando, função ou método específico é executado.</span><span class="sxs-lookup"><span data-stu-id="b8deb-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="b8deb-128">Pontos de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="b8deb-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="b8deb-129">Use um ponto de interrupção de linha de código quando souber a região exata de código que você precisa investigar.</span><span class="sxs-lookup"><span data-stu-id="b8deb-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="b8deb-130">O DevTools sempre pausa antes da execução desta linha de código.</span><span class="sxs-lookup"><span data-stu-id="b8deb-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="b8deb-131">Para definir um ponto de interrupção de linha de código no DevTools:</span><span class="sxs-lookup"><span data-stu-id="b8deb-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="b8deb-132">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-132">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b8deb-133">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="b8deb-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="b8deb-134">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="b8deb-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="b8deb-135">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b8deb-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="b8deb-136">Clique nela.</span><span class="sxs-lookup"><span data-stu-id="b8deb-136">Click on it.</span></span>  <span data-ttu-id="b8deb-137">Um ícone vermelho é exibido ao lado da coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b8deb-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="b8deb-139">Um ponto de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="b8deb-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b8deb-140">Pontos de interrupção de linha de código no código</span><span class="sxs-lookup"><span data-stu-id="b8deb-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="b8deb-141">Execute o `debugger` método do seu código para pausar na linha.</span><span class="sxs-lookup"><span data-stu-id="b8deb-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="b8deb-142">Isso equivale a um [ponto de interrupção de linha de código](#line-of-code-breakpoints), exceto pelo fato de o ponto de interrupção ser definido no seu código, não na interface do usuário do devtools.</span><span class="sxs-lookup"><span data-stu-id="b8deb-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="b8deb-143">Pontos de interrupção de linha de código condicionais</span><span class="sxs-lookup"><span data-stu-id="b8deb-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="b8deb-144">Use um ponto de interrupção de linha de código condicional quando souber a região exata do código que você precisa investigar, mas deseja pausar somente quando outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="b8deb-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="b8deb-145">Para definir um ponto de interrupção de linha de código condicional:</span><span class="sxs-lookup"><span data-stu-id="b8deb-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="b8deb-146">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b8deb-147">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="b8deb-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="b8deb-148">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="b8deb-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="b8deb-149">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b8deb-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="b8deb-150">Clique com o botão direito do mouse no número da linha.</span><span class="sxs-lookup"><span data-stu-id="b8deb-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="b8deb-151">Escolha **Adicionar ponto de interrupção condicional**.</span><span class="sxs-lookup"><span data-stu-id="b8deb-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="b8deb-152">Uma caixa de diálogo é exibida abaixo da linha de código.</span><span class="sxs-lookup"><span data-stu-id="b8deb-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="b8deb-153">Insira sua condição na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b8deb-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="b8deb-154">Selecione `Enter` para ativar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b8deb-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="b8deb-155">Um ícone próximo à coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="b8deb-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="b8deb-157">Um ponto de interrupção de linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="b8deb-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b8deb-158">Gerenciar pontos de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="b8deb-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="b8deb-159">Use o painel **pontos de interrupção** para desabilitar ou remover pontos de interrupção de linha de código de um único local.</span><span class="sxs-lookup"><span data-stu-id="b8deb-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="b8deb-161">O painel **pontos de interrupção**</span><span class="sxs-lookup"><span data-stu-id="b8deb-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="b8deb-162">Marque a caixa de seleção ao lado de uma entrada para desabilitar esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b8deb-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="b8deb-163">Clique com o botão direito do mouse em uma entrada para remover esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b8deb-163">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="b8deb-164">Clique com o botão direito do mouse em qualquer lugar no painel **pontos de interrupção** para desativar todos os pontos de interrupção, desabilitar todos os pontos de interrupção ou remover todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b8deb-164">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="b8deb-165">Desabilitar todos os pontos de interrupção é equivalente a desmarcar cada um deles.</span><span class="sxs-lookup"><span data-stu-id="b8deb-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="b8deb-166">A desativação de todos os pontos de interrupção instrui o DevTools a ignorar todos os pontos de interrupção de linha de código, mas também manter o estado habilitado para que cada um esteja no mesmo estado de antes da reativação de cada um.</span><span class="sxs-lookup"><span data-stu-id="b8deb-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="b8deb-168">Pontos de interrupção desativados no painel **pontos de interrupção**</span><span class="sxs-lookup"><span data-stu-id="b8deb-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b8deb-169">Alterar o DOM dos pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="b8deb-169">DOM change breakpoints</span></span>  

<span data-ttu-id="b8deb-170">Use um ponto de interrupção de alteração DOM quando desejar pausar no código que altera um nó DOM ou filhos.</span><span class="sxs-lookup"><span data-stu-id="b8deb-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="b8deb-171">Para definir um ponto de interrupção de alteração DOM:</span><span class="sxs-lookup"><span data-stu-id="b8deb-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="b8deb-172">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-172">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="b8deb-173">Vá para o elemento no qual você deseja definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b8deb-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="b8deb-174">Clique com o botão direito do mouse no elemento.</span><span class="sxs-lookup"><span data-stu-id="b8deb-174">Right-click the element.</span></span>  
1.  <span data-ttu-id="b8deb-175">Passe o mouse sobre a **pausa**e escolha **modificações de subárvore**, **modificações de atributo**ou remoção de **nó**.</span><span class="sxs-lookup"><span data-stu-id="b8deb-175">Hover over **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="b8deb-177">O menu de contexto para a criação de um ponto de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="b8deb-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b8deb-178">Tipos de pontos de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="b8deb-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="b8deb-179">**Modificações em subárvores**.</span><span class="sxs-lookup"><span data-stu-id="b8deb-179">**Subtree modifications**.</span></span>  <span data-ttu-id="b8deb-180">Disparado quando um filho do nó selecionado no momento é removido ou adicionado, ou o conteúdo de um filho é alterado.</span><span class="sxs-lookup"><span data-stu-id="b8deb-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="b8deb-181">Não disparado em alterações de atributo de nó filho ou em qualquer alteração do nó atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="b8deb-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="b8deb-182">**Modificações de atributos**: disparadas quando um atributo é adicionado ou removido no nó selecionado atualmente ou quando um valor de atributo é alterado.</span><span class="sxs-lookup"><span data-stu-id="b8deb-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="b8deb-183">**Remoção de nó**: disparada quando o nó selecionado no momento é removido.</span><span class="sxs-lookup"><span data-stu-id="b8deb-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="b8deb-184">Pontos de interrupção XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="b8deb-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="b8deb-185">Use um ponto de interrupção XHR quando você quiser interromper quando a URL de solicitação de um XHR contiver uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="b8deb-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="b8deb-186">DevTools pausa na linha de código em que XHR executa o `send()` método.</span><span class="sxs-lookup"><span data-stu-id="b8deb-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="b8deb-187">Esse recurso também funciona com solicitações de [busca de API][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="b8deb-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="b8deb-188">Um exemplo de quando isso é útil é quando você vê que sua página está solicitando uma URL incorreta, e você deseja localizar rapidamente o código-fonte do AJAX ou de busca que está causando a solicitação incorreta.</span><span class="sxs-lookup"><span data-stu-id="b8deb-188">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="b8deb-189">Para definir um ponto de interrupção XHR:</span><span class="sxs-lookup"><span data-stu-id="b8deb-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="b8deb-190">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-190">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b8deb-191">Expanda o painel **pontos de interrupção XHR** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-191">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="b8deb-192">Escolha **Adicionar ponto de interrupção**.</span><span class="sxs-lookup"><span data-stu-id="b8deb-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="b8deb-193">Digite a cadeia de caracteres na qual você deseja interromper.</span><span class="sxs-lookup"><span data-stu-id="b8deb-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="b8deb-194">DevTools pausa quando essa cadeia de caracteres está presente em qualquer lugar em uma URL de solicitação XHR.</span><span class="sxs-lookup"><span data-stu-id="b8deb-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="b8deb-195">Selecione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="b8deb-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="b8deb-197">Criar um ponto de interrupção XHR</span><span class="sxs-lookup"><span data-stu-id="b8deb-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b8deb-198">Pontos de interrupção do ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="b8deb-198">Event listener breakpoints</span></span>   

<span data-ttu-id="b8deb-199">Use pontos de interrupção de ouvinte de eventos quando desejar pausar no código de ouvinte de eventos que é executado após a disparação de um evento.</span><span class="sxs-lookup"><span data-stu-id="b8deb-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="b8deb-200">Você pode selecionar eventos específicos, como `click` , ou categorias de eventos, como todos os eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="b8deb-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="b8deb-201">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-201">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b8deb-202">Expanda o painel **pontos de interrupção de ouvinte de eventos** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-202">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="b8deb-203">DevTools mostra uma lista de categorias de eventos, como **animação**.</span><span class="sxs-lookup"><span data-stu-id="b8deb-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="b8deb-204">Verifique uma dessas categorias para pausar sempre que qualquer evento dessa categoria for acionado ou expandir a categoria e verificar um evento específico.</span><span class="sxs-lookup"><span data-stu-id="b8deb-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="b8deb-206">Criar um ponto de interrupção de ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="b8deb-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b8deb-207">Pontos de interrupção de exceção</span><span class="sxs-lookup"><span data-stu-id="b8deb-207">Exception breakpoints</span></span>  

<span data-ttu-id="b8deb-208">Use pontos de interrupção de exceção quando desejar pausar na linha de código que está lançando uma exceção capturada ou não percebida.</span><span class="sxs-lookup"><span data-stu-id="b8deb-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="b8deb-209">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b8deb-209">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="b8deb-210">Escolha **Pausar nas exceções** \ ( ![ Pausar exceções ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b8deb-210">Choose **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="b8deb-211">O ícone fica azul quando habilitado.</span><span class="sxs-lookup"><span data-stu-id="b8deb-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="b8deb-213">O botão **Pausar exceções**</span><span class="sxs-lookup"><span data-stu-id="b8deb-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b8deb-214">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="b8deb-214">**Optional**.</span></span>  <span data-ttu-id="b8deb-215">Marque a caixa de seleção **Pausar exceções capturadas** se você também quiser pausar em exceções capturadas, além de não capturadas.</span><span class="sxs-lookup"><span data-stu-id="b8deb-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="b8deb-217">Pausado em uma exceção não capturada</span><span class="sxs-lookup"><span data-stu-id="b8deb-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b8deb-218">Pontos de interrupção de função</span><span class="sxs-lookup"><span data-stu-id="b8deb-218">Function breakpoints</span></span>  

<span data-ttu-id="b8deb-219">Execute o `debug(method)` método, onde `method` é o comando, a função ou o método que você deseja depurar, quando desejar pausar sempre que uma função específica for executada.</span><span class="sxs-lookup"><span data-stu-id="b8deb-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="b8deb-220">Você pode inserir `debug()` no seu código (como uma `console.log()` instrução) ou executar o método no console do devtools.</span><span class="sxs-lookup"><span data-stu-id="b8deb-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="b8deb-221">equivale a definir um [ponto de interrupção de linha do código](#line-of-code-breakpoints) na primeira linha da função.</span><span class="sxs-lookup"><span data-stu-id="b8deb-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="b8deb-222">Verifique se a função de destino está em escopo</span><span class="sxs-lookup"><span data-stu-id="b8deb-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="b8deb-223">DevTools lança uma `ReferenceError` se a função que você deseja depurar não está em escopo.</span><span class="sxs-lookup"><span data-stu-id="b8deb-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="b8deb-224">Garantir que a função de destino está em escopo é difícil se você estiver executando o `debug()` método do console devtools.</span><span class="sxs-lookup"><span data-stu-id="b8deb-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="b8deb-225">Aqui está uma estratégia:</span><span class="sxs-lookup"><span data-stu-id="b8deb-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="b8deb-226">Defina um [ponto de interrupção de linha do código](#line-of-code-breakpoints) em um local onde a função esteja no escopo.</span><span class="sxs-lookup"><span data-stu-id="b8deb-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="b8deb-227">Disparar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b8deb-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="b8deb-228">Execute o `debug()` método no console devtools enquanto o código ainda está pausado no ponto de interrupção da linha de código.</span><span class="sxs-lookup"><span data-stu-id="b8deb-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <span data-ttu-id="b8deb-229">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b8deb-229">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introdução à depuração JavaScript no Microsoft Edge DevTools | Documentos da Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar API | MDN"  

> [!NOTE]
> <span data-ttu-id="b8deb-232">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="b8deb-232">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b8deb-233">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b8deb-233">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b8deb-235">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b8deb-235">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
