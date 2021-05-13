---
description: Use a API do Console para gravar mensagens no Console.
title: Referência de API do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 08a29db4dec05de0a21a0e6a9de9a0fb6e0d3f56
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564508"
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
# <a name="console-api-reference"></a>Referência de API do console  

A **ferramenta Console** é útil ao concluir várias tarefas no DevTools.  AS APIs estão disponíveis para incluir em seus scripts. Os métodos de conveniência estão disponíveis apenas para uso na **ferramenta Console,** como `debug()` os métodos `monitorEvents()` e.  Para obter mais informações sobre como começar com **o Console,** navegue até Começar a registrar [mensagens no Console][DevtoolsConsoleConsoleLog].  Para obter mais informações sobre os métodos de conveniência no **Console,** navegue até [Console Utilities API Reference][DevtoolConsoleUtilities].  

---  

## <a name="assert"></a>assert  

Este método grava [um erro](#error) no **Console** quando é avaliada `expression` como `false` .  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.assert(expression, object)
```

[Nível de log][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
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
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="O resultado do exemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         O resultado do `console.assert()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a>clear  

Este método limpa o **Console**.  

Se [o Log de Preservação][DevtoolsConsoleReferenceFilter] estiver ligado, o método [clear](#clear) será desligado.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.clear()
```

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a>Ver também  

*   [Limpar o Console][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

Este método grava o número de vezes que o método [count](#count) foi invocado na mesma linha e com a mesma `label` .  Use o [método countReset](#countreset) para redefinir a contagem.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.count([label])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
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
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="O resultado do exemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         O resultado do `console.count()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a>countReset  

Este método redefine uma contagem.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
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
      Saída
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a>depurar  

Esse método é idêntico ao método [log,](#log) exceto nível de log diferente.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.debug(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Verbose`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="O resultado do exemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         O resultado do `console.debug()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a>dir  

Este método imprime uma representação JSON do objeto especificado.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.dir(object)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="O resultado do exemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         O resultado do `console.dir()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a>dirxml  

Este método imprime uma representação XML dos descendentes de `node` .  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.dirxml(node)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="O resultado do exemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
         O resultado do `console.dirxml()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a>erro  

Este método `object` imprime o para **o Console**, formatará-o como um erro e incluirá um rastreamento de pilha.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.error(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="O resultado do exemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         O resultado do `console.error()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a>agrupar  

Esse método agrupa visualmente mensagens até que o [método groupEnd](#groupend) seja usado.  Use o [método groupCollapsed](#groupcollapsed) para fechar o grupo quando ele registra inicialmente no **Console**.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
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
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="O resultado do exemplo console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         O resultado do `console.group()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

Esse método é idêntico ao [método de log,](#log) exceto que o grupo é recolhido inicialmente quando faz logoff no **Console**.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a>groupEnd  

Esse método interrompe o agrupamento visual de mensagens.  Navegue até o [método group.](#group)  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a>informações  

Esse método é idêntico ao [método log.](#log)  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.info(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="O resultado do exemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         O resultado do `console.info()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a>log  

Este método imprime uma mensagem para o **Console**.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.log(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="O resultado do exemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         O resultado do `console.log()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>tabela  

Este método registra uma matriz de objetos como uma tabela.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.table(array)
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
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
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="O resultado do exemplo console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         O resultado do `console.table()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a>time  

Este método inicia um novo temporizador.  Use o [método timeEnd](#timeend) para parar o temporizador e imprimir o tempo decorrido no **Console**.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
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
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="O resultado do exemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         O resultado do `console.time()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a>timeEnd  

Este método interrompe um temporizador.  Para obter mais informações, navegue até o [método time.](#time)  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.timeEnd([label])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

---  

## <a name="trace"></a>trace  

Este método imprime um rastreamento de pilha para o **Console**.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.trace()
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
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
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="O resultado do exemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         O resultado do `console.trace()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a>warn  

Este método imprime um aviso para o **Console**.  

### <a name="javascript-syntax"></a>Sintaxe JavaScript  

```javascript
console.warn(object [, object, ...])
```  

[Nível de log][DevtoolsConsoleReferencePersist]: `Warning`  

### <a name="javascript-example"></a>Exemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Saída
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="O resultado do exemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
         O resultado do `console.warn()` exemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Logs na ferramenta console | Microsoft Docs"  
[DevtoolConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Limpar o console - console referência | Microsoft Docs"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtrar por nível de registro - referência do console | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Persistir mensagens entre cargas de página - referência de console | Microsoft Docs"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Visão geral das Ferramentas de Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/api) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
