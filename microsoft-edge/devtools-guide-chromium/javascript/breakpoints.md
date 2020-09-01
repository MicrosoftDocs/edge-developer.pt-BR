---
title: Como pausar um código com pontos de interrupção no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 804e864ee3029a49ba1ef2ac1f2deb61c3ba5ec3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983163"
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







# <span data-ttu-id="fdbee-103">Como pausar um código com pontos de interrupção no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fdbee-103">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="fdbee-104">Use pontos de interrupção para pausar o código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fdbee-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="fdbee-105">Este guia explica cada tipo de ponto de interrupção que está disponível no DevTools, bem como quando usar e como definir cada tipo.</span><span class="sxs-lookup"><span data-stu-id="fdbee-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="fdbee-106">Para um tutorial prático do processo de depuração, consulte [introdução à depuração de JavaScript no Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="fdbee-106">For a hands-on tutorial of the debugging process, see [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="fdbee-107">Visão geral de quando usar cada tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="fdbee-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="fdbee-108">O tipo mais conhecido de ponto de interrupção é linha de código.</span><span class="sxs-lookup"><span data-stu-id="fdbee-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="fdbee-109">Mas os pontos de interrupção de linha de código podem ser ineficientemente definidos, especialmente se você não souber exatamente onde procurar ou se estiver trabalhando com uma grande codebase.</span><span class="sxs-lookup"><span data-stu-id="fdbee-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="fdbee-110">Você pode economizar tempo ao depurar sabendo como e quando usar os outros tipos de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="fdbee-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="fdbee-111">Tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="fdbee-111">Breakpoint Type</span></span> | <span data-ttu-id="fdbee-112">Use isso quando desejar pausar...</span><span class="sxs-lookup"><span data-stu-id="fdbee-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="fdbee-113">Linha de código</span><span class="sxs-lookup"><span data-stu-id="fdbee-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="fdbee-114">Em uma região de código exata.</span><span class="sxs-lookup"><span data-stu-id="fdbee-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="fdbee-115">Linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="fdbee-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="fdbee-116">Em uma região de código exata, mas somente quando alguma outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="fdbee-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="fdbee-117">DOM</span><span class="sxs-lookup"><span data-stu-id="fdbee-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="fdbee-118">No código que altera ou remove um nó DOM específico ou os filhos.</span><span class="sxs-lookup"><span data-stu-id="fdbee-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="fdbee-119">XHR</span><span class="sxs-lookup"><span data-stu-id="fdbee-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="fdbee-120">Quando uma URL XHR contém um padrão de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fdbee-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="fdbee-121">Ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="fdbee-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="fdbee-122">No código que é executado após um evento, como `click` , é executado.</span><span class="sxs-lookup"><span data-stu-id="fdbee-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="fdbee-123">Extremamente</span><span class="sxs-lookup"><span data-stu-id="fdbee-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="fdbee-124">Na linha de código que está lançando uma exceção capturada ou não capturada.</span><span class="sxs-lookup"><span data-stu-id="fdbee-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="fdbee-125">Função</span><span class="sxs-lookup"><span data-stu-id="fdbee-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="fdbee-126">Sempre que um comando, função ou método específico é executado.</span><span class="sxs-lookup"><span data-stu-id="fdbee-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="fdbee-127">Pontos de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="fdbee-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="fdbee-128">Use um ponto de interrupção de linha de código quando souber a região exata de código que você precisa investigar.</span><span class="sxs-lookup"><span data-stu-id="fdbee-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="fdbee-129">O DevTools sempre pausa antes da execução desta linha de código.</span><span class="sxs-lookup"><span data-stu-id="fdbee-129">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="fdbee-130">Para definir um ponto de interrupção de linha de código no DevTools:</span><span class="sxs-lookup"><span data-stu-id="fdbee-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="fdbee-131">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="fdbee-132">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="fdbee-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="fdbee-133">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="fdbee-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="fdbee-134">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="fdbee-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="fdbee-135">Clique nela.</span><span class="sxs-lookup"><span data-stu-id="fdbee-135">Click on it.</span></span>  <span data-ttu-id="fdbee-136">Um ícone vermelho é exibido ao lado da coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="fdbee-136">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="fdbee-138">Um ponto de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="fdbee-138">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="fdbee-139">Pontos de interrupção de linha de código no código</span><span class="sxs-lookup"><span data-stu-id="fdbee-139">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="fdbee-140">Execute o `debugger` método do seu código para pausar na linha.</span><span class="sxs-lookup"><span data-stu-id="fdbee-140">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="fdbee-141">Isso equivale a um [ponto de interrupção de linha de código](#line-of-code-breakpoints), exceto pelo fato de o ponto de interrupção ser definido no seu código, não na interface do usuário do devtools.</span><span class="sxs-lookup"><span data-stu-id="fdbee-141">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="fdbee-142">Pontos de interrupção de linha de código condicionais</span><span class="sxs-lookup"><span data-stu-id="fdbee-142">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="fdbee-143">Use um ponto de interrupção de linha de código condicional quando souber a região exata do código que você precisa investigar, mas deseja pausar somente quando outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="fdbee-143">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="fdbee-144">Para definir um ponto de interrupção de linha de código condicional:</span><span class="sxs-lookup"><span data-stu-id="fdbee-144">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="fdbee-145">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-145">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="fdbee-146">Abra o arquivo que contém a linha de código que você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="fdbee-146">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="fdbee-147">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="fdbee-147">Go the line of code.</span></span>  
1.  <span data-ttu-id="fdbee-148">À esquerda da linha de código está a coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="fdbee-148">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="fdbee-149">Clique com o botão direito do mouse no número da linha.</span><span class="sxs-lookup"><span data-stu-id="fdbee-149">Right-click the line number.</span></span>  
1.  <span data-ttu-id="fdbee-150">Selecione **Adicionar ponto de interrupção condicional**.</span><span class="sxs-lookup"><span data-stu-id="fdbee-150">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="fdbee-151">Uma caixa de diálogo é exibida abaixo da linha de código.</span><span class="sxs-lookup"><span data-stu-id="fdbee-151">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="fdbee-152">Insira sua condição na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fdbee-152">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="fdbee-153">Pressione `Enter` para ativar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="fdbee-153">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="fdbee-154">Um ícone próximo à coluna número da linha.</span><span class="sxs-lookup"><span data-stu-id="fdbee-154">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Um ponto de interrupção de linha de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="fdbee-156">Um ponto de interrupção de linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="fdbee-156">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="fdbee-157">Gerenciar pontos de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="fdbee-157">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="fdbee-158">Use o painel **pontos de interrupção** para desabilitar ou remover pontos de interrupção de linha de código de um único local.</span><span class="sxs-lookup"><span data-stu-id="fdbee-158">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="O painel pontos de interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="fdbee-160">O painel **pontos de interrupção**</span><span class="sxs-lookup"><span data-stu-id="fdbee-160">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="fdbee-161">Marque a caixa de seleção ao lado de uma entrada para desabilitar esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="fdbee-161">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="fdbee-162">Clique com o botão direito do mouse em uma entrada para remover esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="fdbee-162">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="fdbee-163">Clique com o botão direito do mouse em qualquer lugar no painel **pontos de interrupção** para desativar todos os pontos de interrupção, desabilitar todos os pontos de interrupção ou remover todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="fdbee-163">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="fdbee-164">Desabilitar todos os pontos de interrupção é equivalente a desmarcar cada um deles.</span><span class="sxs-lookup"><span data-stu-id="fdbee-164">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="fdbee-165">A desativação de todos os pontos de interrupção instrui o DevTools a ignorar todos os pontos de interrupção de linha de código, mas também manter o estado habilitado para que cada um esteja no mesmo estado de antes da reativação de cada um.</span><span class="sxs-lookup"><span data-stu-id="fdbee-165">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Pontos de interrupção desativados no painel pontos de interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="fdbee-167">Pontos de interrupção desativados no painel **pontos de interrupção**</span><span class="sxs-lookup"><span data-stu-id="fdbee-167">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fdbee-168">Alterar o DOM dos pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="fdbee-168">DOM change breakpoints</span></span>   

<span data-ttu-id="fdbee-169">Use um ponto de interrupção de alteração DOM quando desejar pausar no código que altera um nó DOM ou filhos.</span><span class="sxs-lookup"><span data-stu-id="fdbee-169">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="fdbee-170">Para definir um ponto de interrupção de alteração DOM:</span><span class="sxs-lookup"><span data-stu-id="fdbee-170">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="fdbee-171">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-171">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="fdbee-172">Vá para o elemento no qual você deseja definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="fdbee-172">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="fdbee-173">Clique com o botão direito do mouse no elemento.</span><span class="sxs-lookup"><span data-stu-id="fdbee-173">Right-click the element.</span></span>  
1.  <span data-ttu-id="fdbee-174">Passe o mouse sobre a **pausa**e, em seguida, selecione **modificações de subárvore**, **modificações de atributo**ou remoção de **nó**.</span><span class="sxs-lookup"><span data-stu-id="fdbee-174">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="O menu de contexto para a criação de um ponto de interrupção de alteração DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="fdbee-176">O menu de contexto para a criação de um ponto de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="fdbee-176">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="fdbee-177">Tipos de pontos de interrupção de alteração DOM</span><span class="sxs-lookup"><span data-stu-id="fdbee-177">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="fdbee-178">**Modificações em subárvores**.</span><span class="sxs-lookup"><span data-stu-id="fdbee-178">**Subtree modifications**.</span></span>  <span data-ttu-id="fdbee-179">Disparado quando um filho do nó selecionado no momento é removido ou adicionado, ou o conteúdo de um filho é alterado.</span><span class="sxs-lookup"><span data-stu-id="fdbee-179">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="fdbee-180">Não disparado em alterações de atributo de nó filho ou em qualquer alteração do nó atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="fdbee-180">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="fdbee-181">**Modificações de atributos**: disparadas quando um atributo é adicionado ou removido no nó selecionado atualmente ou quando um valor de atributo é alterado.</span><span class="sxs-lookup"><span data-stu-id="fdbee-181">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="fdbee-182">**Remoção de nó**: disparada quando o nó selecionado no momento é removido.</span><span class="sxs-lookup"><span data-stu-id="fdbee-182">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="fdbee-183">Pontos de interrupção XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="fdbee-183">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="fdbee-184">Use um ponto de interrupção XHR quando você quiser interromper quando a URL de solicitação de um XHR contiver uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="fdbee-184">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="fdbee-185">DevTools pausa na linha de código em que XHR executa o `send()` método.</span><span class="sxs-lookup"><span data-stu-id="fdbee-185">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="fdbee-186">Esse recurso também funciona com solicitações de [busca de API][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="fdbee-186">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="fdbee-187">Um exemplo de quando isso é útil é quando você vê que sua página está solicitando uma URL incorreta, e você deseja localizar rapidamente o código-fonte do AJAX ou de busca que está causando a solicitação incorreta.</span><span class="sxs-lookup"><span data-stu-id="fdbee-187">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="fdbee-188">Para definir um ponto de interrupção XHR:</span><span class="sxs-lookup"><span data-stu-id="fdbee-188">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="fdbee-189">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-189">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="fdbee-190">Expanda o painel **pontos de interrupção XHR** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-190">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="fdbee-191">Clique em **Adicionar ponto de interrupção**.</span><span class="sxs-lookup"><span data-stu-id="fdbee-191">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="fdbee-192">Digite a cadeia de caracteres na qual você deseja interromper.</span><span class="sxs-lookup"><span data-stu-id="fdbee-192">Enter the string which you want to break on.</span></span>  <span data-ttu-id="fdbee-193">DevTools pausa quando essa cadeia de caracteres está presente em qualquer lugar em uma URL de solicitação XHR.</span><span class="sxs-lookup"><span data-stu-id="fdbee-193">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="fdbee-194">Pressione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="fdbee-194">Press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Criar um ponto de interrupção XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="fdbee-196">Criar um ponto de interrupção XHR</span><span class="sxs-lookup"><span data-stu-id="fdbee-196">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fdbee-197">Pontos de interrupção do ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="fdbee-197">Event listener breakpoints</span></span> 

<span data-ttu-id="fdbee-198">Use pontos de interrupção de ouvinte de eventos quando desejar pausar no código de ouvinte de eventos que é executado após a disparação de um evento.</span><span class="sxs-lookup"><span data-stu-id="fdbee-198">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="fdbee-199">Você pode selecionar eventos específicos, como `click` , ou categorias de eventos, como todos os eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="fdbee-199">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="fdbee-200">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-200">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="fdbee-201">Expanda o painel **pontos de interrupção de ouvinte de eventos** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-201">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="fdbee-202">DevTools mostra uma lista de categorias de eventos, como **animação**.</span><span class="sxs-lookup"><span data-stu-id="fdbee-202">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="fdbee-203">Verifique uma dessas categorias para pausar sempre que qualquer evento dessa categoria for acionado ou expandir a categoria e verificar um evento específico.</span><span class="sxs-lookup"><span data-stu-id="fdbee-203">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Criar um ponto de interrupção de ouvinte de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="fdbee-205">Criar um ponto de interrupção de ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="fdbee-205">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fdbee-206">Pontos de interrupção de exceção</span><span class="sxs-lookup"><span data-stu-id="fdbee-206">Exception breakpoints</span></span>   

<span data-ttu-id="fdbee-207">Use pontos de interrupção de exceção quando desejar pausar na linha de código que está lançando uma exceção capturada ou não percebida.</span><span class="sxs-lookup"><span data-stu-id="fdbee-207">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="fdbee-208">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-208">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="fdbee-209">Clique em **Pausar nas exceções** \ ( ![ Pausar exceções ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="fdbee-209">Click **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="fdbee-210">O ícone fica azul quando habilitado.</span><span class="sxs-lookup"><span data-stu-id="fdbee-210">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="O botão Pausar exceções" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="fdbee-212">O botão **Pausar exceções**</span><span class="sxs-lookup"><span data-stu-id="fdbee-212">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fdbee-213">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="fdbee-213">**Optional**.</span></span>  <span data-ttu-id="fdbee-214">Marque a caixa de seleção **Pausar exceções capturadas** se você também quiser pausar em exceções capturadas, além de não capturadas.</span><span class="sxs-lookup"><span data-stu-id="fdbee-214">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausado em uma exceção não capturada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="fdbee-216">Pausado em uma exceção não capturada</span><span class="sxs-lookup"><span data-stu-id="fdbee-216">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fdbee-217">Pontos de interrupção de função</span><span class="sxs-lookup"><span data-stu-id="fdbee-217">Function breakpoints</span></span>   

<span data-ttu-id="fdbee-218">Execute o `debug(method)` método, onde `method` é o comando, a função ou o método que você deseja depurar, quando desejar pausar sempre que uma função específica for executada.</span><span class="sxs-lookup"><span data-stu-id="fdbee-218">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="fdbee-219">Você pode inserir `debug()` no seu código (como uma `console.log()` instrução) ou executar o método no console do devtools.</span><span class="sxs-lookup"><span data-stu-id="fdbee-219">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="fdbee-220">equivale a definir um [ponto de interrupção de linha do código](#line-of-code-breakpoints) na primeira linha da função.</span><span class="sxs-lookup"><span data-stu-id="fdbee-220">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="fdbee-221">Verifique se a função de destino está em escopo</span><span class="sxs-lookup"><span data-stu-id="fdbee-221">Make sure the target function is in scope</span></span>   

<span data-ttu-id="fdbee-222">DevTools lança uma `ReferenceError` se a função que você deseja depurar não está em escopo.</span><span class="sxs-lookup"><span data-stu-id="fdbee-222">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="fdbee-223">Garantir que a função de destino está em escopo é difícil se você estiver executando o `debug()` método do console devtools.</span><span class="sxs-lookup"><span data-stu-id="fdbee-223">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="fdbee-224">Aqui está uma estratégia:</span><span class="sxs-lookup"><span data-stu-id="fdbee-224">Here is one strategy:</span></span>  

1.  <span data-ttu-id="fdbee-225">Defina um [ponto de interrupção de linha do código](#line-of-code-breakpoints) em um local onde a função esteja no escopo.</span><span class="sxs-lookup"><span data-stu-id="fdbee-225">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="fdbee-226">Disparar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="fdbee-226">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="fdbee-227">Execute o `debug()` método no console devtools enquanto o código ainda está pausado no ponto de interrupção da linha de código.</span><span class="sxs-lookup"><span data-stu-id="fdbee-227">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introdução à depuração JavaScript no Microsoft Edge DevTools | Documentos da Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar API | MDN"  

> [!NOTE]
> <span data-ttu-id="fdbee-230">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="fdbee-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fdbee-231">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="fdbee-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fdbee-233">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fdbee-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
