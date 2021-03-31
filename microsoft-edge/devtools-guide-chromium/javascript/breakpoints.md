---
description: Saiba mais sobre todas as maneiras de pausar seu código no Microsoft Edge DevTools.
title: Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3d50b7b105aa9a9018ba61e44147f46f3d340079
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439511"
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

# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a><span data-ttu-id="708f7-104">Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="708f7-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="708f7-105">Use pontos de interrupção para pausar seu código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="708f7-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="708f7-106">Este guia explica cada tipo de ponto de interrupção disponível no DevTools, bem como quando usar e como definir cada tipo.</span><span class="sxs-lookup"><span data-stu-id="708f7-106">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="708f7-107">Para obter um tutorial hands-on do processo de depuração, navegue até Introdução à [depuração de JavaScript no Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="708f7-107">For a hands-on tutorial of the debugging process, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <a name="overview-of-when-to-use-each-breakpoint-type"></a><span data-ttu-id="708f7-108">Visão geral de quando usar cada tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="708f7-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="708f7-109">O tipo de ponto de interrupção mais conhecido é a linha de código.</span><span class="sxs-lookup"><span data-stu-id="708f7-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="708f7-110">Mas pontos de interrupção de linha de código podem ser ineficientes para definir, especialmente se você não sabe exatamente onde procurar ou se estiver trabalhando com uma base de código grande.</span><span class="sxs-lookup"><span data-stu-id="708f7-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="708f7-111">Você pode economizar tempo ao depurar sabendo como e quando usar os outros tipos de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="708f7-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="708f7-112">Tipo de ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="708f7-112">Breakpoint Type</span></span> | <span data-ttu-id="708f7-113">Use isso quando quiser pausar...</span><span class="sxs-lookup"><span data-stu-id="708f7-113">Use This When You Want To Pause...</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="708f7-114">Linha de código</span><span class="sxs-lookup"><span data-stu-id="708f7-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="708f7-115">Em uma região exata do código.</span><span class="sxs-lookup"><span data-stu-id="708f7-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="708f7-116">Linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="708f7-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="708f7-117">Em uma região exata do código, mas somente quando alguma outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="708f7-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="708f7-118">DOM</span><span class="sxs-lookup"><span data-stu-id="708f7-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="708f7-119">No código que altera ou remove um nó DOM específico ou os filhos.</span><span class="sxs-lookup"><span data-stu-id="708f7-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="708f7-120">XHR</span><span class="sxs-lookup"><span data-stu-id="708f7-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="708f7-121">Quando uma URL XHR contém um padrão de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="708f7-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="708f7-122">Ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="708f7-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="708f7-123">No código que é executado após um evento, como `click` , é executado.</span><span class="sxs-lookup"><span data-stu-id="708f7-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="708f7-124">Exceção</span><span class="sxs-lookup"><span data-stu-id="708f7-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="708f7-125">Na linha de código que está lançando uma exceção capturada ou não capturada.</span><span class="sxs-lookup"><span data-stu-id="708f7-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="708f7-126">Função</span><span class="sxs-lookup"><span data-stu-id="708f7-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="708f7-127">Sempre que um comando, função ou método específico é executado.</span><span class="sxs-lookup"><span data-stu-id="708f7-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <a name="line-of-code-breakpoints"></a><span data-ttu-id="708f7-128">Pontos de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="708f7-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="708f7-129">Use um ponto de interrupção de linha de código quando você conhecer a região exata do código que precisa investigar.</span><span class="sxs-lookup"><span data-stu-id="708f7-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="708f7-130">O DevTools sempre pausa antes que essa linha de código seja executado.</span><span class="sxs-lookup"><span data-stu-id="708f7-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="708f7-131">Para definir um ponto de interrupção de linha de código no DevTools:</span><span class="sxs-lookup"><span data-stu-id="708f7-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="708f7-132">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="708f7-132">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="708f7-133">Abra o arquivo que contém a linha de código na qual você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="708f7-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="708f7-134">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="708f7-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="708f7-135">À esquerda da linha de código está a coluna de número de linha.</span><span class="sxs-lookup"><span data-stu-id="708f7-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="708f7-136">Escolha-o.</span><span class="sxs-lookup"><span data-stu-id="708f7-136">Choose it.</span></span>  <span data-ttu-id="708f7-137">Um ícone vermelho aparece ao lado da coluna de número de linha.</span><span class="sxs-lookup"><span data-stu-id="708f7-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="708f7-139">Um ponto de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="708f7-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a><span data-ttu-id="708f7-140">Pontos de interrupção de linha de código em seu código</span><span class="sxs-lookup"><span data-stu-id="708f7-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="708f7-141">Execute o `debugger` método do código para pausar nessa linha.</span><span class="sxs-lookup"><span data-stu-id="708f7-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="708f7-142">Isso é equivalente [a](#line-of-code-breakpoints)um ponto de interrupção de linha de código , exceto que o ponto de interrupção está definido em seu código, não na interface do usuário de DevTools.</span><span class="sxs-lookup"><span data-stu-id="708f7-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a><span data-ttu-id="708f7-143">Pontos de interrupção de linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="708f7-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="708f7-144">Use um ponto de interrupção de linha de código condicional quando você conhecer a região exata do código que precisa investigar, mas deseja pausar somente quando alguma outra condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="708f7-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="708f7-145">Para definir um ponto de interrupção de linha de código condicional:</span><span class="sxs-lookup"><span data-stu-id="708f7-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="708f7-146">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="708f7-146">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="708f7-147">Abra o arquivo que contém a linha de código na qual você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="708f7-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="708f7-148">Vá para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="708f7-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="708f7-149">À esquerda da linha de código está a coluna de número de linha.</span><span class="sxs-lookup"><span data-stu-id="708f7-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="708f7-150">Passe o mouse no número da linha e abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="708f7-150">Hover on the line number and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="708f7-151">Escolha **Adicionar ponto de interrupção condicional**.</span><span class="sxs-lookup"><span data-stu-id="708f7-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="708f7-152">Uma caixa de diálogo é exibida abaixo da linha de código.</span><span class="sxs-lookup"><span data-stu-id="708f7-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="708f7-153">Insira sua condição na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="708f7-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="708f7-154">Selecione `Enter` para ativar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="708f7-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="708f7-155">Um ícone ao lado da coluna de número de linha.</span><span class="sxs-lookup"><span data-stu-id="708f7-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Um ponto de interrupção de linha de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="708f7-157">Um ponto de interrupção de linha de código condicional</span><span class="sxs-lookup"><span data-stu-id="708f7-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a><span data-ttu-id="708f7-158">Gerenciar pontos de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="708f7-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="708f7-159">Use o **painel Pontos de Interrupção** para desabilitar ou remover pontos de interrupção de linha de código de um único local.</span><span class="sxs-lookup"><span data-stu-id="708f7-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="O painel Pontos de Interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="708f7-161">O **painel Pontos de** Interrupção</span><span class="sxs-lookup"><span data-stu-id="708f7-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="708f7-162">Marque a caixa de seleção ao lado de uma entrada para desabilitar esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="708f7-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="708f7-163">Passe o mouse em uma entrada e abra o menu contextual \(clique com o botão direito do mouse\) para remover esse ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="708f7-163">Hover on an entry and open the contextual menu \(right-click\) to remove that breakpoint.</span></span>  
*   <span data-ttu-id="708f7-164">Passe o  mouse em qualquer lugar no painel Pontos de Interrupção e abra o menu contextual \(clique com o botão direito do mouse\) para desativar todos os pontos de interrupção, desabilitar todos os pontos de interrupção ou remover todos os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="708f7-164">Hover anywhere in the **Breakpoints** pane and open the contextual menu \(right-click\) to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="708f7-165">Desabilitar todos os pontos de interrupção equivale a desmarcar cada um deles.</span><span class="sxs-lookup"><span data-stu-id="708f7-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="708f7-166">Desativar todos os pontos de interrupção instrui o DevTools a ignorar todos os pontos de interrupção de linha de código, mas também manter o estado habilitado para que cada um esteja no mesmo estado de antes quando você reativar cada um deles.</span><span class="sxs-lookup"><span data-stu-id="708f7-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Pontos de interrupção desativados no painel Pontos de Interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="708f7-168">Pontos de interrupção desativados no painel **Pontos de** Interrupção</span><span class="sxs-lookup"><span data-stu-id="708f7-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a><span data-ttu-id="708f7-169">Pontos de interrupção de alteração dom</span><span class="sxs-lookup"><span data-stu-id="708f7-169">DOM change breakpoints</span></span>  

<span data-ttu-id="708f7-170">Use um ponto de interrupção de alteração dom quando quiser pausar o código que altera um nó DOM ou os filhos.</span><span class="sxs-lookup"><span data-stu-id="708f7-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="708f7-171">Para definir um ponto de interrupção de alteração dom:</span><span class="sxs-lookup"><span data-stu-id="708f7-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="708f7-172">Escolha a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="708f7-172">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="708f7-173">Vá para o elemento no qual você deseja definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="708f7-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="708f7-174">Passe o mouse no elemento e abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="708f7-174">Hover on the element and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="708f7-175">Hover on **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span><span class="sxs-lookup"><span data-stu-id="708f7-175">Hover on **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="O menu de contexto para criar um ponto de interrupção de alteração dom" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="708f7-177">O menu de contexto para criar um ponto de interrupção de alteração dom</span><span class="sxs-lookup"><span data-stu-id="708f7-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a><span data-ttu-id="708f7-178">Tipos de pontos de interrupção de alteração dom</span><span class="sxs-lookup"><span data-stu-id="708f7-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="708f7-179">**Modificações de subárvore**.</span><span class="sxs-lookup"><span data-stu-id="708f7-179">**Subtree modifications**.</span></span>  <span data-ttu-id="708f7-180">Disparado quando um filho do nó selecionado no momento é removido ou adicionado, ou o conteúdo de um filho é alterado.</span><span class="sxs-lookup"><span data-stu-id="708f7-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="708f7-181">Não acionada em alterações de atributo de nó filho ou em quaisquer alterações no nó selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="708f7-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="708f7-182">**Modificações de atributos**: disparado quando um atributo é adicionado ou removido no nó selecionado no momento ou quando um valor de atributo é modificado.</span><span class="sxs-lookup"><span data-stu-id="708f7-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="708f7-183">**Remoção do**nó : disparado quando o nó selecionado no momento é removido.</span><span class="sxs-lookup"><span data-stu-id="708f7-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <a name="xhrfetch-breakpoints"></a><span data-ttu-id="708f7-184">Pontos de interrupção XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="708f7-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="708f7-185">Use um ponto de interrupção XHR quando quiser quebrar quando a URL de solicitação de um XHR contiver uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="708f7-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="708f7-186">O DevTools pausa na linha de código em que o XHR executa o `send()` método.</span><span class="sxs-lookup"><span data-stu-id="708f7-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="708f7-187">Esse recurso também funciona com [solicitações de API de][MDNFetchApi] Busca.</span><span class="sxs-lookup"><span data-stu-id="708f7-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="708f7-188">Um exemplo de quando isso é útil é quando sua página da Web está solicitando uma URL incorreta e você deseja encontrar rapidamente o código-fonte AJAX ou Fetch que está causando a solicitação incorreta.</span><span class="sxs-lookup"><span data-stu-id="708f7-188">One example of when this is helpful is when your webpage is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="708f7-189">Para definir um ponto de interrupção XHR:</span><span class="sxs-lookup"><span data-stu-id="708f7-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="708f7-190">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="708f7-190">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="708f7-191">Expanda o **painel Pontos de Interrupção XHR.**</span><span class="sxs-lookup"><span data-stu-id="708f7-191">Expand the **XHR Breakpoints** panel.</span></span>  
1.  <span data-ttu-id="708f7-192">Escolha **Adicionar ponto de interrupção**.</span><span class="sxs-lookup"><span data-stu-id="708f7-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="708f7-193">Insira a cadeia de caracteres na qual você deseja quebrar.</span><span class="sxs-lookup"><span data-stu-id="708f7-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="708f7-194">O DevTools pausa quando essa cadeia de caracteres está presente em qualquer lugar em uma URL de solicitação XHR.</span><span class="sxs-lookup"><span data-stu-id="708f7-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="708f7-195">Selecione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="708f7-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Criar um ponto de interrupção XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="708f7-197">Criar um ponto de interrupção XHR</span><span class="sxs-lookup"><span data-stu-id="708f7-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a><span data-ttu-id="708f7-198">Pontos de interrupção do ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="708f7-198">Event listener breakpoints</span></span>  

<span data-ttu-id="708f7-199">Use pontos de interrupção do ouvinte de eventos quando quiser pausar o código do ouvinte de eventos que é executado após um evento ser disparado.</span><span class="sxs-lookup"><span data-stu-id="708f7-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="708f7-200">Você pode selecionar eventos específicos, como `click` , ou categorias de eventos, como todos os eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="708f7-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="708f7-201">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="708f7-201">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="708f7-202">Expanda o **painel Pontos de Interrupção do Ouvinte de** Eventos.</span><span class="sxs-lookup"><span data-stu-id="708f7-202">Expand the **Event Listener Breakpoints** panel.</span></span>  <span data-ttu-id="708f7-203">DevTools mostra uma lista de categorias de eventos, como **Animação**.</span><span class="sxs-lookup"><span data-stu-id="708f7-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="708f7-204">Verifique uma dessas categorias para pausar sempre que qualquer evento dessa categoria for acionado ou expanda a categoria e verifique um evento específico.</span><span class="sxs-lookup"><span data-stu-id="708f7-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Criar um ponto de interrupção do ouvinte de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="708f7-206">Criar um ponto de interrupção do ouvinte de eventos</span><span class="sxs-lookup"><span data-stu-id="708f7-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a><span data-ttu-id="708f7-207">Pontos de interrupção de exceção</span><span class="sxs-lookup"><span data-stu-id="708f7-207">Exception breakpoints</span></span>  

<span data-ttu-id="708f7-208">Use pontos de interrupção de exceção quando quiser pausar na linha de código que está lançando uma exceção capturada ou não capturada.</span><span class="sxs-lookup"><span data-stu-id="708f7-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="708f7-209">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="708f7-209">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="708f7-210">Escolha **Pausar em exceções** \( Pause on ![ exceptions ](../media/pause-on-exceptions-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="708f7-210">Choose **Pause on exceptions** \(![Pause on exceptions](../media/pause-on-exceptions-icon.msft.png)\).</span></span>  <span data-ttu-id="708f7-211">O ícone fica azul quando habilitado.</span><span class="sxs-lookup"><span data-stu-id="708f7-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="O botão Pausar exceções" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="708f7-213">O **botão Pausar exceções**</span><span class="sxs-lookup"><span data-stu-id="708f7-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="708f7-214">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="708f7-214">**Optional**.</span></span>  <span data-ttu-id="708f7-215">Marque a **caixa de seleção Pausar** Exceções Capturadas se você também quiser pausar em exceções capturadas, além de exceções não capturadas.</span><span class="sxs-lookup"><span data-stu-id="708f7-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausada em uma exceção não acatada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="708f7-217">Pausada em uma exceção não acatada</span><span class="sxs-lookup"><span data-stu-id="708f7-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <a name="function-breakpoints"></a><span data-ttu-id="708f7-218">Pontos de interrupção de função</span><span class="sxs-lookup"><span data-stu-id="708f7-218">Function breakpoints</span></span>  

<span data-ttu-id="708f7-219">Execute o método, onde está o comando, a função ou o método que você deseja depurar, quando quiser pausar sempre que `debug(method)` uma função específica for `method` executado.</span><span class="sxs-lookup"><span data-stu-id="708f7-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="708f7-220">Você pode inserir em seu código (como uma instrução) ou executar `debug()` o método no Console de `console.log()` DevTools.</span><span class="sxs-lookup"><span data-stu-id="708f7-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="708f7-221">equivale a definir um [ponto de interrupção de](#line-of-code-breakpoints) linha de código na primeira linha da função.</span><span class="sxs-lookup"><span data-stu-id="708f7-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a><span data-ttu-id="708f7-222">Certifique-se de que a função de destino está no escopo</span><span class="sxs-lookup"><span data-stu-id="708f7-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="708f7-223">DevTools lança um se a `ReferenceError` função que você deseja depurar não estiver no escopo.</span><span class="sxs-lookup"><span data-stu-id="708f7-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="708f7-224">A garantia de que a função de destino está no escopo é complicada se você estiver executando o método no `debug()` Console de DevTools.</span><span class="sxs-lookup"><span data-stu-id="708f7-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="708f7-225">Aqui está uma estratégia:</span><span class="sxs-lookup"><span data-stu-id="708f7-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="708f7-226">De definir [um ponto de interrupção de linha de código](#line-of-code-breakpoints) em algum lugar onde a função está no escopo.</span><span class="sxs-lookup"><span data-stu-id="708f7-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="708f7-227">Acionar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="708f7-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="708f7-228">Execute o `debug()` método no Console de DevTools enquanto o código ainda está pausado no ponto de interrupção de linha de código.</span><span class="sxs-lookup"><span data-stu-id="708f7-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="708f7-229">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="708f7-229">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar api | MDN"  

> [!NOTE]
> <span data-ttu-id="708f7-232">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="708f7-232">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="708f7-233">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="708f7-233">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="708f7-235">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="708f7-235">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
