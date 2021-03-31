---
description: Use a API do Console para gravar mensagens no Console.
title: Referência da API de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f38a7403cf11fbec5f5833fc0b1ed10207b436de
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398046"
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

# <a name="console-api-reference"></a><span data-ttu-id="24397-104">Referência da API de console</span><span class="sxs-lookup"><span data-stu-id="24397-104">Console API reference</span></span>  

<span data-ttu-id="24397-105">Use os métodos da API do Console para gravar mensagens no Console do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24397-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="24397-106">Para obter uma introdução interativa ao tópico, navegue até [Introdução a Mensagens em Log para o Console][DevtoolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="24397-106">For an interactive introduction to the topic, navigate to [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="24397-107">Para os métodos de conveniência, como ou que estão disponíveis apenas no painel console, navegue até Referência da `debug()` `monitorEvents()` API de [Utilitários de Console][DevtoolConsoleUtilities]. </span><span class="sxs-lookup"><span data-stu-id="24397-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="24397-108">assert</span><span class="sxs-lookup"><span data-stu-id="24397-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="24397-109">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="24397-110">Grava um [erro](#error) no console quando `expression` é avaliada como `false` .</span><span class="sxs-lookup"><span data-stu-id="24397-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="O resultado do exemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="24397-112">Figura 1: O resultado do `console.assert()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="24397-113">clear</span><span class="sxs-lookup"><span data-stu-id="24397-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="24397-114">Limpa o console.</span><span class="sxs-lookup"><span data-stu-id="24397-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="24397-115">Se [Preserve Log][DevtoolsConsoleReferenceLevel] estiver habilitado, o método [clear](#clear) será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="24397-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <a name="see-also"></a><span data-ttu-id="24397-116">Veja também</span><span class="sxs-lookup"><span data-stu-id="24397-116">See also</span></span>  

*   [<span data-ttu-id="24397-117">Limpar o Console</span><span class="sxs-lookup"><span data-stu-id="24397-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="24397-118">count</span><span class="sxs-lookup"><span data-stu-id="24397-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="24397-119">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-120">Grava o número de vezes que o [método count](#count) foi invocado na mesma linha e com a mesma `label` .</span><span class="sxs-lookup"><span data-stu-id="24397-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="24397-121">Use o [método countReset](#countreset) para redefinir a contagem.</span><span class="sxs-lookup"><span data-stu-id="24397-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="O resultado do exemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="24397-123">Figura 2: O resultado do `console.count()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="24397-124">countReset</span><span class="sxs-lookup"><span data-stu-id="24397-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="24397-125">Redefine uma contagem.</span><span class="sxs-lookup"><span data-stu-id="24397-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a><span data-ttu-id="24397-126">depurar</span><span class="sxs-lookup"><span data-stu-id="24397-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="24397-127">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="24397-128">Idêntico ao [log,](#log) exceto nível de log diferente.</span><span class="sxs-lookup"><span data-stu-id="24397-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="O resultado do exemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="24397-130">Figura 3: O resultado do `console.debug()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <a name="dir"></a><span data-ttu-id="24397-131">dir</span><span class="sxs-lookup"><span data-stu-id="24397-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="24397-132">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-133">Imprime uma representação JSON do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="24397-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="O resultado do exemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="24397-135">Figura 4: O resultado do `console.dir()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="24397-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="24397-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="24397-137">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-138">Imprime uma representação XML dos descendentes de `node` .</span><span class="sxs-lookup"><span data-stu-id="24397-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="O resultado do exemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="24397-140">Figura 5: O resultado do `console.dirxml()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <a name="error"></a><span data-ttu-id="24397-141">erro</span><span class="sxs-lookup"><span data-stu-id="24397-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="24397-142">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="24397-143">`object`Imprime o para o Console, formatará-o como um erro e incluirá um rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="24397-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="O resultado do exemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="24397-145">Figura 6: O resultado do `console.error()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <a name="group"></a><span data-ttu-id="24397-146">agrupar</span><span class="sxs-lookup"><span data-stu-id="24397-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="24397-147">Agrupa visualmente mensagens até que o [método groupEnd](#groupend) seja usado.</span><span class="sxs-lookup"><span data-stu-id="24397-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="24397-148">Use o [método groupCollapsed](#groupcollapsed) para fechar o grupo quando ele for registrado inicialmente no Console.</span><span class="sxs-lookup"><span data-stu-id="24397-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="O resultado do exemplo console.group()" lightbox="../media/console-demo-group-button.msft.png":::
   <span data-ttu-id="24397-150">Figura 7: O resultado do `console.group()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="24397-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="24397-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="24397-152">O mesmo que o [método de log,](#log) exceto que o grupo é recolhido inicialmente quando ele é registrado no Console.</span><span class="sxs-lookup"><span data-stu-id="24397-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <a name="groupend"></a><span data-ttu-id="24397-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="24397-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="24397-154">Interrompe o agrupamento visual de mensagens.</span><span class="sxs-lookup"><span data-stu-id="24397-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="24397-155">Navegue até o [método group.](#group)</span><span class="sxs-lookup"><span data-stu-id="24397-155">Navigate to the [group](#group) method.</span></span>  

---  

## <a name="info"></a><span data-ttu-id="24397-156">informações</span><span class="sxs-lookup"><span data-stu-id="24397-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="24397-157">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-158">Idêntico ao método [log.](#log)</span><span class="sxs-lookup"><span data-stu-id="24397-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="O resultado do exemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="24397-160">Figura 8: O resultado do `console.info()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <a name="log"></a><span data-ttu-id="24397-161">log</span><span class="sxs-lookup"><span data-stu-id="24397-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="24397-162">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-163">Imprime uma mensagem no Console.</span><span class="sxs-lookup"><span data-stu-id="24397-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="O resultado do exemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="24397-165">Figura 9: O resultado do `console.log()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <a name="table"></a><span data-ttu-id="24397-166">table</span><span class="sxs-lookup"><span data-stu-id="24397-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="24397-167">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-168">Registra uma matriz de objetos como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="24397-168">Logs an array of objects as a table.</span></span>  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="O resultado do exemplo console.table()" lightbox="../media/console-demo-table-button.msft.png":::
   <span data-ttu-id="24397-170">Figura 10: O resultado do `console.table()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <a name="time"></a><span data-ttu-id="24397-171">time</span><span class="sxs-lookup"><span data-stu-id="24397-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="24397-172">Inicia um novo temporizador.</span><span class="sxs-lookup"><span data-stu-id="24397-172">Starts a new timer.</span></span>  <span data-ttu-id="24397-173">Use o [método timeEnd](#timeend) para parar o temporizador e imprimir o tempo decorrido no Console.</span><span class="sxs-lookup"><span data-stu-id="24397-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="O resultado do exemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="24397-175">Figura 11: O resultado do `console.time()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="24397-176">timeEnd</span><span class="sxs-lookup"><span data-stu-id="24397-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="24397-177">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-178">Interrompe um timer.</span><span class="sxs-lookup"><span data-stu-id="24397-178">Stops a timer.</span></span>  <span data-ttu-id="24397-179">Navegue até o [método time.](#time)</span><span class="sxs-lookup"><span data-stu-id="24397-179">Navigate to the [time](#time) method.</span></span>  

---  

## <a name="trace"></a><span data-ttu-id="24397-180">trace</span><span class="sxs-lookup"><span data-stu-id="24397-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="24397-181">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="24397-182">Imprime um rastreamento de pilha no Console.</span><span class="sxs-lookup"><span data-stu-id="24397-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="O resultado do exemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="24397-184">Figura 12: O resultado do `console.trace()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <a name="warn"></a><span data-ttu-id="24397-185">warn</span><span class="sxs-lookup"><span data-stu-id="24397-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="24397-186">[Nível de log][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="24397-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="24397-187">Imprime um aviso no Console.</span><span class="sxs-lookup"><span data-stu-id="24397-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="O resultado do exemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="24397-189">Figura 13: O resultado do `console.warn()` exemplo</span><span class="sxs-lookup"><span data-stu-id="24397-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="24397-190">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="24397-190">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Começar a registrar mensagens no console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência da API de Utilitários de Console"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Limpar o Console - Referência do Console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Persistir mensagens entre cargas de página - Referência do Console"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nível de log - Referência do console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

> [!NOTE]
> <span data-ttu-id="24397-197">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="24397-197">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="24397-198">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/api) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="24397-198">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="24397-200">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="24397-200">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
