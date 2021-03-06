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

# <a name="console-api-reference"></a>Referência da API de console  

Use os métodos da API do Console para gravar mensagens no Console do JavaScript.  Para obter uma introdução interativa ao tópico, navegue até [Introdução a Mensagens em Log para o Console][DevtoolsConsoleLog].  Para os métodos de conveniência, como ou que estão disponíveis apenas no painel console, navegue até Referência da `debug()` `monitorEvents()` API de [Utilitários de Console][DevtoolConsoleUtilities]. ****  

---  

## <a name="assert"></a>assert  

```javascript
console.assert(expression, object)
```

[Nível de log][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Grava um [erro](#error) no console quando `expression` é avaliada como `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="O resultado do exemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   Figura 1: O resultado do `console.assert()` exemplo  
:::image-end:::  

---  

## <a name="clear"></a>clear  

```javascript
console.clear()
```

Limpa o console.  

```javascript
console.clear();  
```  

Se [Preserve Log][DevtoolsConsoleReferenceLevel] estiver habilitado, o método [clear](#clear) será desabilitado.  

### <a name="see-also"></a>Veja também  

*   [Limpar o Console][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

```javascript
console.count([label])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Grava o número de vezes que o [método count](#count) foi invocado na mesma linha e com a mesma `label` .  Use o [método countReset](#countreset) para redefinir a contagem.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="O resultado do exemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   Figura 2: O resultado do `console.count()` exemplo  
:::image-end:::  

---  

## <a name="countreset"></a>countReset  

```javascript
console.countReset([label])
```  

Redefine uma contagem.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a>depurar  

```javascript
console.debug(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Verbose`

Idêntico ao [log,](#log) exceto nível de log diferente.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="O resultado do exemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   Figura 3: O resultado do `console.debug()` exemplo  
:::image-end:::  

---  

## <a name="dir"></a>dir  

```javascript
console.dir(object)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime uma representação JSON do objeto especificado.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="O resultado do exemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   Figura 4: O resultado do `console.dir()` exemplo  
:::image-end:::  

---  

## <a name="dirxml"></a>dirxml  

```javascript
console.dirxml(node)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime uma representação XML dos descendentes de `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="O resultado do exemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Figura 5: O resultado do `console.dirxml()` exemplo  
:::image-end:::  

---  

## <a name="error"></a>erro  

```javascript
console.error(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Error`  

`object`Imprime o para o Console, formatará-o como um erro e incluirá um rastreamento de pilha.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="O resultado do exemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   Figura 6: O resultado do `console.error()` exemplo  
:::image-end:::  

---  

## <a name="group"></a>agrupar  

```javascript
console.group(label)
```  

Agrupa visualmente mensagens até que o [método groupEnd](#groupend) seja usado.  Use o [método groupCollapsed](#groupcollapsed) para fechar o grupo quando ele for registrado inicialmente no Console.  

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
   Figura 7: O resultado do `console.group()` exemplo  
:::image-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

O mesmo que o [método de log,](#log) exceto que o grupo é recolhido inicialmente quando ele é registrado no Console.  

---  

## <a name="groupend"></a>groupEnd  

```javascript
console.groupEnd(label)
```  

Interrompe o agrupamento visual de mensagens.  Navegue até o [método group.](#group)  

---  

## <a name="info"></a>informações  

```javascript
console.info(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Idêntico ao método [log.](#log)  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="O resultado do exemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   Figura 8: O resultado do `console.info()` exemplo  
:::image-end:::  

---  

## <a name="log"></a>log  

```javascript
console.log(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime uma mensagem no Console.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="O resultado do exemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   Figura 9: O resultado do `console.log()` exemplo  
:::image-end:::  

---  

## <a name="table"></a>table  

```javascript
console.table(array)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Registra uma matriz de objetos como uma tabela.  

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
   Figura 10: O resultado do `console.table()` exemplo  
:::image-end:::  

---  

## <a name="time"></a>time  

```javascript
console.time([label])
```  

Inicia um novo temporizador.  Use o [método timeEnd](#timeend) para parar o temporizador e imprimir o tempo decorrido no Console.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="O resultado do exemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   Figura 11: O resultado do `console.time()` exemplo  
:::image-end:::  

---  

## <a name="timeend"></a>timeEnd  

```javascript
console.timeEnd([label])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Interrompe um timer.  Navegue até o [método time.](#time)  

---  

## <a name="trace"></a>trace  

```javascript
console.trace()
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime um rastreamento de pilha no Console.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="O resultado do exemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   Figura 12: O resultado do `console.trace()` exemplo  
:::image-end:::  

---  

## <a name="warn"></a>warn  

```javascript
console.warn(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Warning`  

Imprime um aviso no Console.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="O resultado do exemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   Figura 13: O resultado do `console.warn()` exemplo  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Começar a registrar mensagens no console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência da API de Utilitários de Console"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Limpar o Console - Referência do Console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Persistir mensagens entre cargas de página - Referência do Console"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nível de log - Referência do console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/api) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
