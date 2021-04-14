---
description: Use a API do Console para gravar mensagens no Console.
title: Referência de API do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 54b89e25501449a1e5119afa812a0535fbc6ffbb
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483251"
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
# <a name="console-api-reference"></a><span data-ttu-id="0f8be-104">Referência de API do console</span><span class="sxs-lookup"><span data-stu-id="0f8be-104">Console API reference</span></span>  

<span data-ttu-id="0f8be-105">A **ferramenta Console** é útil ao concluir várias tarefas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f8be-105">The **Console** tool is helpful when you complete multiple tasks in the DevTools.</span></span>  <span data-ttu-id="0f8be-106">AS APIs estão disponíveis para incluir em seus scripts.</span><span class="sxs-lookup"><span data-stu-id="0f8be-106">APIs are available to include in your scripts.</span></span> <span data-ttu-id="0f8be-107">Os métodos de conveniência estão disponíveis apenas para uso na **ferramenta Console,** como `debug()` os métodos `monitorEvents()` e.</span><span class="sxs-lookup"><span data-stu-id="0f8be-107">Convenience methods are only available for use in the **Console** tool, such as the `debug()` and `monitorEvents()` methods.</span></span>  <span data-ttu-id="0f8be-108">Para obter mais informações sobre como começar com **o Console,** navegue até Começar a registrar [mensagens no Console][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="0f8be-108">For more information on getting started with the **Console**, navigate to [Get started with logging messages to the Console][DevtoolsConsoleConsoleLog].</span></span>  <span data-ttu-id="0f8be-109">Para obter mais informações sobre os métodos de conveniência no **Console,** navegue até [Console Utilities API Reference][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="0f8be-109">For more information on the convenience methods in the **Console**, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="0f8be-110">assert</span><span class="sxs-lookup"><span data-stu-id="0f8be-110">assert</span></span>  

<span data-ttu-id="0f8be-111">Este método grava [um erro](#error) no **Console** quando é avaliada `expression` como `false` .</span><span class="sxs-lookup"><span data-stu-id="0f8be-111">This method writes an [error](#error) to the **Console** when `expression` evaluates to `false`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-112">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-112">JavaScript syntax</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="0f8be-113">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-113">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-114">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-114">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-115">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-115">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const x = 5;
      const y = 3;
      const reason = 'x is expected to be less than y';
      console.assert(x < y, {x, y, reason});
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-116">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-116">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="O resultado do exemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         <span data-ttu-id="0f8be-118">O resultado do `console.assert()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-118">The result of the `console.assert()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a><span data-ttu-id="0f8be-119">clear</span><span class="sxs-lookup"><span data-stu-id="0f8be-119">clear</span></span>  

<span data-ttu-id="0f8be-120">Este método limpa o **Console**.</span><span class="sxs-lookup"><span data-stu-id="0f8be-120">This method clears the **Console**.</span></span>  

<span data-ttu-id="0f8be-121">Se [o Log de Preservação][DevtoolsConsoleReferenceFilter] estiver ligado, o método [clear](#clear) será desligado.</span><span class="sxs-lookup"><span data-stu-id="0f8be-121">If [Preserve Log][DevtoolsConsoleReferenceFilter] is turned on, the [clear](#clear) method is turned off.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-122">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-122">JavaScript syntax</span></span>  

```javascript
console.clear()
```

### <a name="javascript-example"></a><span data-ttu-id="0f8be-123">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-123">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-124">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-124">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-125">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-125">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a><span data-ttu-id="0f8be-126">Ver também</span><span class="sxs-lookup"><span data-stu-id="0f8be-126">See also</span></span>  

*   [<span data-ttu-id="0f8be-127">Limpar o Console</span><span class="sxs-lookup"><span data-stu-id="0f8be-127">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="0f8be-128">count</span><span class="sxs-lookup"><span data-stu-id="0f8be-128">count</span></span>  

<span data-ttu-id="0f8be-129">Este método grava o número de vezes que o método [count](#count) foi invocado na mesma linha e com a mesma `label` .</span><span class="sxs-lookup"><span data-stu-id="0f8be-129">This method writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="0f8be-130">Use o [método countReset](#countreset) para redefinir a contagem.</span><span class="sxs-lookup"><span data-stu-id="0f8be-130">Use the [countReset](#countreset) method to reset the count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-131">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-131">JavaScript syntax</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="0f8be-132">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-133">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-133">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-134">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.count();
      console.count('coffee');
      console.count();
      console.count();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-135">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-135">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="O resultado do exemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         <span data-ttu-id="0f8be-137">O resultado do `console.count()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-137">The result of the `console.count()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="0f8be-138">countReset</span><span class="sxs-lookup"><span data-stu-id="0f8be-138">countReset</span></span>  

<span data-ttu-id="0f8be-139">Este método redefine uma contagem.</span><span class="sxs-lookup"><span data-stu-id="0f8be-139">This method resets a count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-140">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-140">JavaScript syntax</span></span>  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-141">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-141">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-142">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.countReset();
      console.countReset('coffee');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-143">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-143">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a><span data-ttu-id="0f8be-144">depurar</span><span class="sxs-lookup"><span data-stu-id="0f8be-144">debug</span></span>  

<span data-ttu-id="0f8be-145">Esse método é idêntico ao método [log,](#log) exceto nível de log diferente.</span><span class="sxs-lookup"><span data-stu-id="0f8be-145">This method is identical to the [log](#log) method, except different log level.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-146">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-146">JavaScript syntax</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="0f8be-147">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-147">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-148">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-148">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-149">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-150">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-150">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="O resultado do exemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         <span data-ttu-id="0f8be-152">O resultado do `console.debug()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-152">The result of the `console.debug()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a><span data-ttu-id="0f8be-153">dir</span><span class="sxs-lookup"><span data-stu-id="0f8be-153">dir</span></span>  

<span data-ttu-id="0f8be-154">Este método imprime uma representação JSON do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="0f8be-154">This method prints a JSON representation of the specified object.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-155">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-155">JavaScript syntax</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="0f8be-156">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-156">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-157">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-157">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-158">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-159">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-159">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="O resultado do exemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         <span data-ttu-id="0f8be-161">O resultado do `console.dir()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-161">The result of the `console.dir()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="0f8be-162">dirxml</span><span class="sxs-lookup"><span data-stu-id="0f8be-162">dirxml</span></span>  

<span data-ttu-id="0f8be-163">Este método imprime uma representação XML dos descendentes de `node` .</span><span class="sxs-lookup"><span data-stu-id="0f8be-163">This method prints an XML representation of the descendants of `node`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-164">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-164">JavaScript syntax</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="0f8be-165">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-165">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-166">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-166">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-167">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-167">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-168">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-168">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="O resultado do exemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
         <span data-ttu-id="0f8be-170">O resultado do `console.dirxml()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-170">The result of the `console.dirxml()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a><span data-ttu-id="0f8be-171">erro</span><span class="sxs-lookup"><span data-stu-id="0f8be-171">error</span></span>  

<span data-ttu-id="0f8be-172">Este método `object` imprime o para **o Console**, formatará-o como um erro e incluirá um rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="0f8be-172">This method prints the `object` to the **Console**, formats it as an error, and includes a stack trace.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-173">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-173">JavaScript syntax</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="0f8be-174">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-175">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-175">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-176">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-177">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-177">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="O resultado do exemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         <span data-ttu-id="0f8be-179">O resultado do `console.error()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-179">The result of the `console.error()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a><span data-ttu-id="0f8be-180">agrupar</span><span class="sxs-lookup"><span data-stu-id="0f8be-180">group</span></span>  

<span data-ttu-id="0f8be-181">Esse método agrupa visualmente mensagens até que o [método groupEnd](#groupend) seja usado.</span><span class="sxs-lookup"><span data-stu-id="0f8be-181">This method visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="0f8be-182">Use o [método groupCollapsed](#groupcollapsed) para fechar o grupo quando ele registra inicialmente no **Console**.</span><span class="sxs-lookup"><span data-stu-id="0f8be-182">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it initially logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-183">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-183">JavaScript syntax</span></span>  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-184">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-184">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-185">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const label = 'Adolescent Irradiated Espionage Tortoises';
      console.group(label);
      console.info('Leo');
      console.info('Mike');
      console.info('Don');
      console.info('Raph');
      console.groupEnd(label);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-186">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-186">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="O resultado do exemplo console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         <span data-ttu-id="0f8be-188">O resultado do `console.group()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-188">The result of the `console.group()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="0f8be-189">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="0f8be-189">groupCollapsed</span></span>  

<span data-ttu-id="0f8be-190">Esse método é idêntico ao [método de log,](#log) exceto que o grupo é recolhido inicialmente quando faz logoff no **Console**.</span><span class="sxs-lookup"><span data-stu-id="0f8be-190">This method is identical to the [log](#log) method, except the group is initially collapsed when it logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-191">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-191">JavaScript syntax</span></span>  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a><span data-ttu-id="0f8be-192">groupEnd</span><span class="sxs-lookup"><span data-stu-id="0f8be-192">groupEnd</span></span>  

<span data-ttu-id="0f8be-193">Esse método interrompe o agrupamento visual de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0f8be-193">This method stops visually grouping messages.</span></span>  <span data-ttu-id="0f8be-194">Navegue até o [método group.](#group)</span><span class="sxs-lookup"><span data-stu-id="0f8be-194">Navigate to the [group](#group) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-195">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-195">JavaScript syntax</span></span>  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a><span data-ttu-id="0f8be-196">informações</span><span class="sxs-lookup"><span data-stu-id="0f8be-196">info</span></span>  

<span data-ttu-id="0f8be-197">Esse método é idêntico ao [método log.](#log)</span><span class="sxs-lookup"><span data-stu-id="0f8be-197">This method is identical to the [log](#log) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-198">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-198">JavaScript syntax</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="0f8be-199">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-199">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-200">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-200">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-201">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-202">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-202">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="O resultado do exemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         <span data-ttu-id="0f8be-204">O resultado do `console.info()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-204">The result of the `console.info()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a><span data-ttu-id="0f8be-205">log</span><span class="sxs-lookup"><span data-stu-id="0f8be-205">log</span></span>  

<span data-ttu-id="0f8be-206">Este método imprime uma mensagem para o **Console**.</span><span class="sxs-lookup"><span data-stu-id="0f8be-206">This method prints a message to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-207">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-207">JavaScript syntax</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="0f8be-208">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-208">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-209">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-209">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-210">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-211">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-211">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="O resultado do exemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         <span data-ttu-id="0f8be-213">O resultado do `console.log()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-213">The result of the `console.log()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="0f8be-214">table</span><span class="sxs-lookup"><span data-stu-id="0f8be-214">table</span></span>  

<span data-ttu-id="0f8be-215">Este método registra uma matriz de objetos como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="0f8be-215">This method logs an array of objects as a table.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-216">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-216">JavaScript syntax</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="0f8be-217">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-217">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-218">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-218">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-219">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-219">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.table([
          {
              first: 'René',
              last: 'Magritte',
          },
          {
              first: 'Chaim',
              last: 'Soutine',
              birthday: '18930113',
          },
          {
              first: 'Henri',
              last: 'Matisse',
          }
      ]);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-220">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-220">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="O resultado do exemplo console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         <span data-ttu-id="0f8be-222">O resultado do `console.table()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-222">The result of the `console.table()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a><span data-ttu-id="0f8be-223">time</span><span class="sxs-lookup"><span data-stu-id="0f8be-223">time</span></span>  

<span data-ttu-id="0f8be-224">Este método inicia um novo temporizador.</span><span class="sxs-lookup"><span data-stu-id="0f8be-224">This method starts a new timer.</span></span>  <span data-ttu-id="0f8be-225">Use o [método timeEnd](#timeend) para parar o temporizador e imprimir o tempo decorrido no **Console**.</span><span class="sxs-lookup"><span data-stu-id="0f8be-225">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-226">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-226">JavaScript syntax</span></span>  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-227">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-227">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-228">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.time();
      for (var i = 0; i < 100000; i++) {
          let square = i ** 2;
      }
      console.timeEnd();
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-229">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-229">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="O resultado do exemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         <span data-ttu-id="0f8be-231">O resultado do `console.time()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-231">The result of the `console.time()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="0f8be-232">timeEnd</span><span class="sxs-lookup"><span data-stu-id="0f8be-232">timeEnd</span></span>  

<span data-ttu-id="0f8be-233">Este método interrompe um temporizador.</span><span class="sxs-lookup"><span data-stu-id="0f8be-233">This method stops a timer.</span></span>  <span data-ttu-id="0f8be-234">Para obter mais informações, navegue até o [método time.](#time)</span><span class="sxs-lookup"><span data-stu-id="0f8be-234">For more information, navigate to the [time](#time) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-235">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-235">JavaScript syntax</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="0f8be-236">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-236">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

---  

## <a name="trace"></a><span data-ttu-id="0f8be-237">trace</span><span class="sxs-lookup"><span data-stu-id="0f8be-237">trace</span></span>  

<span data-ttu-id="0f8be-238">Este método imprime um rastreamento de pilha para o **Console**.</span><span class="sxs-lookup"><span data-stu-id="0f8be-238">This method prints a stack trace to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-239">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-239">JavaScript syntax</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="0f8be-240">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-240">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-241">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-241">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-242">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-242">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const first = () => { second(); };
      const second = () => { third(); };
      const third = () => { fourth(); };
      const fourth = () => { console.trace(); };
      first();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-243">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-243">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="O resultado do exemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         <span data-ttu-id="0f8be-245">O resultado do `console.trace()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-245">The result of the `console.trace()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a><span data-ttu-id="0f8be-246">warn</span><span class="sxs-lookup"><span data-stu-id="0f8be-246">warn</span></span>  

<span data-ttu-id="0f8be-247">Este método imprime um aviso para o **Console**.</span><span class="sxs-lookup"><span data-stu-id="0f8be-247">This method prints a warning to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="0f8be-248">Sintaxe JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-248">JavaScript syntax</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="0f8be-249">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="0f8be-249">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

### <a name="javascript-example"></a><span data-ttu-id="0f8be-250">Exemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f8be-250">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f8be-251">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="0f8be-252">Saída</span><span class="sxs-lookup"><span data-stu-id="0f8be-252">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="O resultado do exemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
         <span data-ttu-id="0f8be-254">O resultado do `console.warn()` exemplo</span><span class="sxs-lookup"><span data-stu-id="0f8be-254">The result of the `console.warn()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0f8be-255">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0f8be-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Logs na ferramenta console | Microsoft Docs"  
[DevtoolConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Limpar o console - console referência | Microsoft Docs"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtrar por nível de registro - referência do console | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Persistir mensagens entre cargas de página - referência de console | Microsoft Docs"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Visão geral das Ferramentas de Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="0f8be-262">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0f8be-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0f8be-263">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/api) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="0f8be-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0f8be-265">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0f8be-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
