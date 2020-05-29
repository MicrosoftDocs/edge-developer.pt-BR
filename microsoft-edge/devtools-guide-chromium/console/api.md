---
title: Referência de API do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: e54bae7c7c61584ccd39568f1bb54312cc2082c0
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601751"
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





# Referência de API do console   

  

Use os métodos da API do console para escrever mensagens no console a partir de seu JavaScript.  Consulte Introdução ao [registro de mensagens ao console][DevtoolsConsoleLog] para obter uma introdução interativa ao tópico.  Consulte [referência da API de utilitários de console] [DevtoolConsoleUtilities] se você estiver procurando por métodos de conveniência, como `debug()` ou `monitorEvents()` que estão disponíveis apenas no console.  

## indica  

```javascript
console.assert(expression, object)
```

[Nível de log][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Grava um [erro](#error) no console durante `expression` a avaliação `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### Figura 1  
> O resultado do `console.assert()` exemplo  
> ![O resultado do exemplo console. Assert ()][ImageAssert]  

## elimina  

```javascript
console.clear()
```

Limpa o console.  

```javascript
console.clear();  
```  

Se a [preservação do log][DevtoolsConsoleReferenceLevel] estiver habilitada, o método [limpar](#clear) estará desabilitado.  

Consulte também: [limpar o console][DevtoolsConsoleReferenceClear]  

## contador  

```javascript
console.count([label])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Grava o número de vezes que o método de [contagem](#count) foi invocado na mesma linha e com o mesmo `label` .  Use o método [countReset](#countreset) para redefinir a contagem.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### Figura 2  
> O resultado do `console.count()` exemplo  
> ![O resultado do exemplo console. Count ()][ImageCount]  

## countReset  

```javascript
console.countReset([label])
```  

Redefine uma contagem.  

```javascript
console.countReset();
console.countReset('coffee');
```  

## depurar  

```javascript
console.debug(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Idêntico ao método [log](#log) .  

```javascript
console.debug('debug');  
```  

> ##### Figura 3  
> O resultado do `console.debug()` exemplo  
> ![O resultado do exemplo console. debug ()][ImageDebug]  

## dir  

```javascript
console.dir(object)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime uma representação JSON do objeto especificado.  

```javascript
console.dir(document.head);
```  

> ##### Figura 4  
> O resultado do `console.dir()` exemplo  
> ![O resultado do exemplo console. dir ()][ImageDir]  

## dirxml  

```javascript
console.dirxml(node)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime uma representação XML dos descendentes `node` .  

```javascript
console.dirxml(document);
```  

> ##### Figura 5  
> O resultado do `console.dirxml()` exemplo  
> ![O resultado do exemplo console. DirXML ()][ImageDirXml]  

## erro  

```javascript
console.error(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Error`  

Imprime o `object` console do, formata-o como um erro e inclui um rastreamento de pilha.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### Figura 6  
> O resultado do `console.error()` exemplo  
> ![O resultado do exemplo de console. Error ()][ImageError]  

## agrupar  

```javascript
console.group(label)
```  

Visualmente agrupar mensagens até que o método [groupEnd](#groupend) seja usado.  Use o método [groupCollapsed](#groupcollapsed) para recolher o grupo quando ele for inicialmente registrado no console.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### Figura 7  
> O resultado do `console.group()` exemplo  
> ![O resultado do exemplo console. Group ()][ImageGroup]  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Mesmo que o método [log](#log) , exceto que o grupo é inicialmente recolhido quando ele é registrado no console.  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Interrompe o agrupamento visual de mensagens.  Consulte o método [grupo](#group) .  

## informações  

```javascript
console.info(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Idêntico ao método [log](#log) .  

```javascript
console.info('info');
```  

> ##### Figura 8  
> O resultado do `console.info()` exemplo  
> ![O resultado do exemplo de console.info ()][ImageInfo]  

## efetua  

```javascript
console.log(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime uma mensagem no console.  

```javascript
console.log('log');
```  

> ##### Figura 9  
> O resultado do `console.log()` exemplo  
> ![O resultado do exemplo console. log ()][ImageLog]  

## TableName  

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

> ##### Figura 10  
> O resultado do `console.table()` exemplo  
> ![O resultado do exemplo console. Table ()][ImageTable]  

## time  

```javascript
console.time([label])
```  

Inicia um novo temporizador.  Use o método [timeEnd](#timeend) para interromper o temporizador e imprimir o tempo decorrido no console.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### Figura 11  
> O resultado do `console.time()` exemplo  
> ![O resultado do exemplo de console. time ()][ImageTime]  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Interrompe um temporizador.  Consulte o método [time](#time) .  

## rastreia  

```javascript
console.trace()
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

Imprime um rastreamento de pilha no console.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### Figura 12  
> O resultado do `console.trace()` exemplo  
> ![O resultado do exemplo console. Trace ()][ImageTrace]  

## avisá  

```javascript
console.warn(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Warning`  

Imprime um aviso no console.  

```javascript
console.warn('warn');
```  

> ##### Figura 13  
> O resultado do `console.warn()` exemplo  
> ![O resultado do exemplo console. Warn ()][ImageWarn]  

   

  

<!-- image links -->  

[ImageAssert]: /microsoft-edge/devtools-guide-chromium/media/console-demo-assert-button.msft.png "Figura 1: o resultado do exemplo de console. Assert ()"  
[ImageCount]: /microsoft-edge/devtools-guide-chromium/media/console-demo-count-button.msft.png "Figura 2: o resultado do exemplo console. Count ()"  
[ImageDebug]: /microsoft-edge/devtools-guide-chromium/media/console-demo-debug-button.msft.png "Figura 3: o resultado do exemplo de console. debug ()"  
[ImageDir]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dir-button.msft.png "Figura 4: o resultado do exemplo de console. dir ()"  
[ImageDirXml]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dirxml-button.msft.png "Figura 5: o resultado do exemplo console. DirXML ()"  
[ImageError]: /microsoft-edge/devtools-guide-chromium/media/console-demo-error-button.msft.png "Figura 6: o resultado do exemplo de console. Error ()"  
[ImageGroup]: /microsoft-edge/devtools-guide-chromium/media/console-demo-group-button.msft.png "Figura 7: o resultado do exemplo de console. Group ()"  
[ImageInfo]: /microsoft-edge/devtools-guide-chromium/media/console-demo-info-button.msft.png "Figura 8: o resultado do exemplo de console.info ()"  
[ImageLog]: /microsoft-edge/devtools-guide-chromium/media/console-demo-log-button.msft.png "Figura 9: o resultado do exemplo console. log ()"  
[ImageTable]: /microsoft-edge/devtools-guide-chromium/media/console-demo-table-button.msft.png "Figura 10: o resultado do exemplo de console. Table ()"  
[ImageTime]: /microsoft-edge/devtools-guide-chromium/media/console-demo-time-button.msft.png "Figura 11: o resultado do exemplo de console. tempo ()"  
[ImageTrace]: /microsoft-edge/devtools-guide-chromium/media/console-demo-trace-button.msft.png "Figura 12: o resultado do exemplo de console. Trace ()"  
[ImageWarn]: /microsoft-edge/devtools-guide-chromium/media/console-demo-warn-button.msft.png "Figura 13: o resultado do exemplo console. Warn ()"  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência de API de utilitários de console"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Limpar o console-referência do console"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Mensagens de persistência nas cargas de página – referência do console"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nível de log – referência do console"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/api) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
