---
description: Usar a API do console para depurar e criar o perfil do seu código de forma programática
title: DevTools-console-API do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, API do console
ms.custom: seodec18
ms.openlocfilehash: d722934c3694c3c23e367141158ad45f6d03b175
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562261"
---
# API do console

A *API do console* fornece acesso programático e linha de comando ao console do devtools por meio do `console` objeto global, permitindo que você:

 - [Registrar mensagens personalizadas](#logging-custom-messages) a partir de seu código
 - [Inspecionar objetos e elementos](#inspecting-objects-and-elements) e registrar suas informações
 - [Testar e medir o código](#testing-and-measuring) definindo asserções, temporizadores e contadores
 - [Criar instantâneos do heap](#taking-heap-snapshots) para avaliar o consumo de memória do seu código em execução e identificar vazamentos de memória
 - [Rastrear suas chamadas de chamadas](#tracing-callstacks) para entender para onde o seu código está sendo chamado 
 - [Organize a saída do log](#organizing-log-output) para simplificar a depuração

Veja a seguir os comandos e os parâmetros de formatação aos quais o Microsoft Edge oferece suporte no momento. Elas funcionam de maneira semelhante nos principais navegadores.

## Registrando mensagens personalizadas

Seu código pode enviar vários tipos de mensagens personalizadas para o console, incluindo:

Tipo de mensagem  | &nbsp;   |
:------------------- | :------ |
[**Error ()**](https://developer.mozilla.org/docs/Web/API/Console/error) e [ **Exception ()**](https://developer.mozilla.org/docs/Web/API/Console/error)| Erros críticos e falhas
[**WARN ()**](https://developer.mozilla.org/docs/Web/API/Console/warn) | Possíveis erros ou comportamento inesperado 
[**info ()**](https://developer.mozilla.org/docs/Web/API/Console/info) | Informações úteis, mas não críticas
[**log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) e [ **debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log) | Depuração geral (sem gerar um ícone de alerta do sistema no console)

   
Você pode agrupá-los e filtrá-los com as outras mensagens geradas pelo Microsoft Edge no painel do console. Todos os métodos de mensagens personalizados exigem um parâmetro de cadeia de caracteres (mensagem) e parâmetros de substituição de formato opcionais. O Microsoft Edge suporta as seguintes opções de formatação:

Parâmetro de formato | &nbsp;
:------------------- | :--- |
**% b** | Binário
**% c** | Estilo CSS embutido (consulte o exemplo abaixo)
**% d**, **% i** | Inteiro 
**% f** | Float  
**% s** | String 
**% x** | Decimal 
**% e** | Expoente 

Por exemplo, veja como você deve incluir variáveis de cadeia de caracteres e inteiros na mensagem de registro:

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

Veja como você pode adicionar um efeito de realce verde a uma mensagem de log com CSS embutido ( `%c` ):

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Log de console com estilos embutidos](../media/console_api_css.png)

## Inspecionando objetos e elementos

Objetos inspecionáveis aparecem no console em um modo de exibição de árvore recolhido com nós expansíveis. O console detecta se você está enviando um nó DOM (como um div) ou um objeto JavaScript (como um evento) e os exibe automaticamente como o tipo detectado.

Você também pode forçar uma saída específica:

Comando | &nbsp;
:------------------- | :--- |
[**Dir ()**](https://developer.mozilla.org/docs/Web/API/Console/dir) | Exibe como objeto JavaScript inspecionável
[**dirxml()**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | Exibe como nó DOM inspecionável

Por exemplo, tente abrir o console e comparar as seguintes saídas do `<div id='main'>` elemento nesta página:

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Comparação da saída ' dir ' versus ' DirXML '](../media/console_api_dir.png)

### Selecionando um elemento no painel **elementos**

Você pode selecionar um elemento dentro do contexto da árvore HTML da página diretamente do console para o layout imediato e a depuração de estilo.

Comando | &nbsp;
:------------------- | :--- |
**Select ()** | Alterna para o painel **elementos** e define o foco para o elemento especificado.

Por exemplo, se você abrir o console nesta página e digitar:

```javascript
console.select(document.querySelector("body"));
```

O DevTools mudará para o painel **elementos** (se ele ainda não for o atual) e definirá o foco no [*modo de exibição de árvore HTML*](../elements.md#html-tree-view) para o elemento especificado.

![Exemplo do método ' Select '](../media/console_api_select.png)

## Teste e medição

### Testando seu código

Adicione declarações de teste de API de console ao seu código para teste de unidade e depuração do seu código à medida que ele é executado no navegador.

Comando | &nbsp;
:------------ | :-------------
[**Assert ()**](https://developer.mozilla.org/docs/Web/API/Console/assert) | Registra uma mensagem de erro do console se a expressão fornecida for avaliada como *false*.

Além da expressão lógica fornecida como a asserção testada, você pode adicionar uma mensagem opcional e parâmetros de formatação como usaria com outras [mensagens de console personalizadas](#logging-custom-messages). Por exemplo:

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Exemplo do método ' Assert '](../media/console_api_assert.png)

### Contando execuções em seu código

Você pode definir contadores em seu código para controlar quantas vezes o código ao redor é executado. Os contadores de configuração podem ajudar a garantir que o seu código esteja sendo executado como esperado e ajudá-lo a diagnosticar afunilamentos de desempenho.

Comando | &nbsp;
:------------ | :-------------
[**Count ()**](https://developer.mozilla.org/docs/Web/API/Console/count) | Incrementa e registra o número de vezes que a contagem de horários *()* para o rótulo especificado foi executada.
[**countReset()**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | Redefine a contagem para zero para o rótulo do contador fornecido.

Por exemplo, executar as seguintes linhas no console:

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 . . . fará:
> Meu contador: 1

### Cronometrar seu código

Instrumente seu código com temporizadores rotulados para medir quanto tempo leva para concluir uma determinada operação.

Comando | &nbsp;
:------------ | :-------------
[**tempo ()**](https://developer.mozilla.org/docs/Web/API/Console/time) | Inicia um temporizador com o rótulo fornecido.
[**timeEnd()**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | Termina o temporizador com o rótulo fornecido e informa o tempo decorrido (em milissegundos).
[**Carimbo de data/hora ()**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | Relata a hora atual do sistema (em milissegundos).

Por exemplo, tente executar as seguintes linhas no console:

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### Fazendo instantâneos de heap

Faça instantâneos do heap para avaliar o consumo de memória do seu código em execução e identificar vazamentos de memória.

Comando | &nbsp;
:------------ | :-------------
**takeHeapSnapshot()** | Captura detalhes sobre o heap JavaScript atual e seus objetos alocados.

O DevTools de [memória](../memory.md#toolbar) do deve estar em execução para fazer instantâneos de heap. Cada instantâneo será exibido como um bloco no [*Resumo do instantâneo*](../memory.md#snapshot-summary) do painel [**memória**](../memory.md) para inspeção adicional.

## Rastreamento de chamadas de rastreamento

Compreender onde o código está sendo chamado, qual código está em execução e por quanto tempo essa execução pode ser útil para analisar slowness ou comportamento inesperado. Um rastreamento de pilha mostra o caminho de execução que o código levou para contatá-lo, da solicitação de rastreamento para cima até o caminho. 

Comando | &nbsp;
:------------ | :-------------
[**Trace ()**](https://developer.mozilla.org/docs/Web/API/Console/trace) | Gera um rastreamento da pilha de execução de script atual.

Por exemplo, executar o seguinte código no console:

```javascript
function a(){
  c();
}
function b(){
  c();
}
function c(){
  console.trace()
}
function d(){
  b();
}

a();
d();
```

. . . produzirá os seguintes rastreamentos de pilha:
> console. Trace () em c (código de avaliação: 8:3) em um (código eval: 2:3) no código eval (código eval: 14:1)
> 
> console. Trace () em c (código eval: 8:3) at b (código eval: 5:3) at d (código eval: 11:3) no código eval (código eval: 15:1)

## Organizando a saída do log

Para desmarcar toda a saída de console anterior, use *console. Clear ()* (ou `CTRL + L` ). Isso não desmarca a BackStack do histórico de comandos do seu console (você ainda pode percorrendo as teclas de seta para cima e para baixo).

Comando | &nbsp;
:------------ | :-------------
[**Clear ()**](https://developer.mozilla.org/docs/Web/API/Console/clear) | Limpa toda a saída de console anterior.

Se o seu código produzir muitas mensagens de console, você pode organizá-las visualmente em blocos aninhados com os seguintes comandos:

 Comando | &nbsp;
:------------ | :-------------
[**Group ()**](https://developer.mozilla.org/docs/Web/API/Console/group) | Inicia um novo nível de aninhamento para saída do console com o rótulo especificado (opcional).
[**groupCollapsed()**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | Inicia um novo nível de aninhamento para saída de console com o rótulo especificado (opcional), no entanto, o controle de agrupamento é recolhido por padrão e deve ser expandido (clicando no controle de seta) para exibir a saída filho.
[**groupEnd()**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | Finaliza o grupo de aninhamento para o rótulo especificado.

Por exemplo, tente digitar os seguintes comandos no console:

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

. . . em seguida, expanda os controles *Group 1* e *Group 1,1* para ver como os comentários do log são aninhados:

![Agrupando mensagens no console](../media/console_api_group.png)

Às vezes, é mais fácil visualizar um objeto ou matriz JavaScript em formato de tabela, em vez de uma lista plana. Para isso, você pode usar o comando *console. Table ()* :

Comando | &nbsp;
:------------ | :-------------
[**Table ()**](https://developer.mozilla.org/docs/Web/API/Console/table) | Gera a matriz ou o objeto fornecido ao console em formato tabular.

Por exemplo, a seguinte matriz de objeto:

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

. . . será renderizado como esta tabela no console:

![Exibir uma matriz de objetos como uma tabela no console](../media/console_api_table.png)
