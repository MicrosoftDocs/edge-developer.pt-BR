---
description: Use a API do console para escrever mensagens no console.
title: Referência de API do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 684c0a1e42357ceca0a0295859e64447251f191a
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993251"
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

# <span data-ttu-id="df4b8-104">Referência de API do console</span><span class="sxs-lookup"><span data-stu-id="df4b8-104">Console API Reference</span></span>  

<span data-ttu-id="df4b8-105">Use os métodos da API do console para escrever mensagens no console a partir de seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="df4b8-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="df4b8-106">Para obter uma introdução interativa ao tópico, consulte Introdução ao [registro de mensagens no console][DevtoolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="df4b8-106">For an interactive introduction to the topic, see [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="df4b8-107">Para os métodos de conveniência como `debug()` ou `monitorEvents()` que estão disponíveis apenas no painel do **console** , consulte referência da API de [utilitários de console][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="df4b8-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, see [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <span data-ttu-id="df4b8-108">indica</span><span class="sxs-lookup"><span data-stu-id="df4b8-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="df4b8-109">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="df4b8-110">Grava um [erro](#error) no console durante `expression` a avaliação `false` .</span><span class="sxs-lookup"><span data-stu-id="df4b8-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="O resultado do exemplo console. Assert ()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="df4b8-112">Figura 1: o resultado do `console.assert()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-113">elimina</span><span class="sxs-lookup"><span data-stu-id="df4b8-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="df4b8-114">Limpa o console.</span><span class="sxs-lookup"><span data-stu-id="df4b8-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="df4b8-115">Se a [preservação do log][DevtoolsConsoleReferenceLevel] estiver habilitada, o método [limpar](#clear) estará desabilitado.</span><span class="sxs-lookup"><span data-stu-id="df4b8-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <span data-ttu-id="df4b8-116">Ver também</span><span class="sxs-lookup"><span data-stu-id="df4b8-116">See also</span></span>  

*   [<span data-ttu-id="df4b8-117">Limpar o console</span><span class="sxs-lookup"><span data-stu-id="df4b8-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <span data-ttu-id="df4b8-118">contador</span><span class="sxs-lookup"><span data-stu-id="df4b8-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="df4b8-119">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-120">Grava o número de vezes que o método de [contagem](#count) foi invocado na mesma linha e com o mesmo `label` .</span><span class="sxs-lookup"><span data-stu-id="df4b8-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="df4b8-121">Use o método [countReset](#countreset) para redefinir a contagem.</span><span class="sxs-lookup"><span data-stu-id="df4b8-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="O resultado do exemplo console. Count ()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="df4b8-123">Figura 2: o resultado do `console.count()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-124">countReset</span><span class="sxs-lookup"><span data-stu-id="df4b8-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="df4b8-125">Redefine uma contagem.</span><span class="sxs-lookup"><span data-stu-id="df4b8-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <span data-ttu-id="df4b8-126">depurar</span><span class="sxs-lookup"><span data-stu-id="df4b8-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="df4b8-127">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="df4b8-128">Idêntico ao [log](#log) , exceto o nível de log diferente.</span><span class="sxs-lookup"><span data-stu-id="df4b8-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="O resultado do exemplo console. debug ()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="df4b8-130">Figura 3: o resultado do `console.debug()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-131">dir</span><span class="sxs-lookup"><span data-stu-id="df4b8-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="df4b8-132">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-133">Imprime uma representação JSON do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="df4b8-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="O resultado do exemplo console. dir ()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="df4b8-135">Figura 4: o resultado do `console.dir()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="df4b8-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="df4b8-137">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-138">Imprime uma representação XML dos descendentes `node` .</span><span class="sxs-lookup"><span data-stu-id="df4b8-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="O resultado do exemplo console. DirXML ()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="df4b8-140">Figura 5: o resultado do `console.dirxml()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-141">erro</span><span class="sxs-lookup"><span data-stu-id="df4b8-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="df4b8-142">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="df4b8-143">Imprime o `object` console do, formata-o como um erro e inclui um rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="df4b8-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="O resultado do exemplo de console. Error ()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="df4b8-145">Figura 6: o resultado do `console.error()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-146">agrupar</span><span class="sxs-lookup"><span data-stu-id="df4b8-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="df4b8-147">Visualmente agrupar mensagens até que o método [groupEnd](#groupend) seja usado.</span><span class="sxs-lookup"><span data-stu-id="df4b8-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="df4b8-148">Use o método [groupCollapsed](#groupcollapsed) para recolher o grupo quando ele for inicialmente registrado no console.</span><span class="sxs-lookup"><span data-stu-id="df4b8-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="O resultado do exemplo console. Group ()" lightbox="../media/console-demo-group-button.msft.png":::
   <span data-ttu-id="df4b8-150">Figura 7: o resultado do `console.group()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="df4b8-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="df4b8-152">Mesmo que o método [log](#log) , exceto que o grupo é inicialmente recolhido quando ele é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="df4b8-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <span data-ttu-id="df4b8-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="df4b8-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="df4b8-154">Interrompe o agrupamento visual de mensagens.</span><span class="sxs-lookup"><span data-stu-id="df4b8-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="df4b8-155">Consulte o método [grupo](#group) .</span><span class="sxs-lookup"><span data-stu-id="df4b8-155">See the [group](#group) method.</span></span>  

---  

## <span data-ttu-id="df4b8-156">informações</span><span class="sxs-lookup"><span data-stu-id="df4b8-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="df4b8-157">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-158">Idêntico ao método [log](#log) .</span><span class="sxs-lookup"><span data-stu-id="df4b8-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="O resultado do exemplo de console.info ()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="df4b8-160">Figura 8: o resultado do `console.info()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-161">efetua</span><span class="sxs-lookup"><span data-stu-id="df4b8-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="df4b8-162">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-163">Imprime uma mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="df4b8-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="O resultado do exemplo console. log ()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="df4b8-165">Figura 9: o resultado do `console.log()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-166">TableName</span><span class="sxs-lookup"><span data-stu-id="df4b8-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="df4b8-167">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-168">Registra uma matriz de objetos como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="df4b8-168">Logs an array of objects as a table.</span></span>  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="O resultado do exemplo console. Table ()" lightbox="../media/console-demo-table-button.msft.png":::
   <span data-ttu-id="df4b8-170">Figura 10: o resultado do `console.table()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-171">time</span><span class="sxs-lookup"><span data-stu-id="df4b8-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="df4b8-172">Inicia um novo temporizador.</span><span class="sxs-lookup"><span data-stu-id="df4b8-172">Starts a new timer.</span></span>  <span data-ttu-id="df4b8-173">Use o método [timeEnd](#timeend) para interromper o temporizador e imprimir o tempo decorrido no console.</span><span class="sxs-lookup"><span data-stu-id="df4b8-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="O resultado do exemplo de console. time ()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="df4b8-175">Figura 11: o resultado do `console.time()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-176">timeEnd</span><span class="sxs-lookup"><span data-stu-id="df4b8-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="df4b8-177">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-178">Interrompe um temporizador.</span><span class="sxs-lookup"><span data-stu-id="df4b8-178">Stops a timer.</span></span>  <span data-ttu-id="df4b8-179">Consulte o método [time](#time) .</span><span class="sxs-lookup"><span data-stu-id="df4b8-179">See the [time](#time) method.</span></span>  

---  

## <span data-ttu-id="df4b8-180">rastreia</span><span class="sxs-lookup"><span data-stu-id="df4b8-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="df4b8-181">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="df4b8-182">Imprime um rastreamento de pilha no console.</span><span class="sxs-lookup"><span data-stu-id="df4b8-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="O resultado do exemplo console. Trace ()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="df4b8-184">Figura 12: o resultado do `console.trace()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="df4b8-185">avisá</span><span class="sxs-lookup"><span data-stu-id="df4b8-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="df4b8-186">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="df4b8-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="df4b8-187">Imprime um aviso no console.</span><span class="sxs-lookup"><span data-stu-id="df4b8-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="O resultado do exemplo console. Warn ()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="df4b8-189">Figura 13: o resultado do `console.warn()` exemplo</span><span class="sxs-lookup"><span data-stu-id="df4b8-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência de API de utilitários de console"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Limpar o console-referência do console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Mensagens de persistência nas cargas de página – referência do console"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nível de log – referência do console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

> [!NOTE]
> <span data-ttu-id="df4b8-196">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="df4b8-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="df4b8-197">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/api) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="df4b8-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="df4b8-199">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="df4b8-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
