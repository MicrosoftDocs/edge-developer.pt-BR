---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio do Tempo de Execução.  O domínio de tempo de execução expõe o tempo de execução do JavaScript por meio de objetos de avaliação remota e espelho.  Os resultados da avaliação são retornados como objeto espelho que expõe o tipo de objeto, a representação de cadeia de caracteres e o identificador exclusivo que pode ser usado para referência de objeto posterior.  Os objetos originais são mantidos na memória, a menos que sejam lançados explicitamente.
title: Domínio do tempo de execução - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397689"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a>Domínio do tempo de execução - DevTools Protocol Versão 0.1 (EdgeHTML)  

O domínio de tempo de execução expõe o tempo de execução do JavaScript por meio de objetos de avaliação remota e espelho.  Os resultados da avaliação são retornados como objeto espelho que expõe o tipo de objeto, a representação de cadeia de caracteres e o identificador exclusivo que pode ser usado para referência de objeto posterior.  Os objetos originais são mantidos na memória, a menos que sejam lançados explicitamente.  

| Classificação | Membros |  
|:--- |:--- |  
| [Métodos](#methods) | [enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties) |  
| [Eventos](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |  
| [Tipos](#types) | [ScriptId,](#scriptid) [RemoteObjectId,](#remoteobjectid) [UnserializableValue,](#unserializablevalue) [RemoteObject,](#remoteobject) [PropertyDescriptor,](#propertydescriptor) [CallArgument,](#callargument) [ExecutionContextId,](#executioncontextid) [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |  

## <a name="methods"></a>Métodos  

### <a name="enable"></a>Habilitar  

Habilita o relatório do `executionContextsCleared` evento.  

&nbsp;  

---  

### <a name="disable"></a>Desabilitar   

Desabilita o relatório do `executionContextsCleared` evento.  

&nbsp;  

---  

### <a name="evaluate"></a>evaluate  

Avalia a expressão no objeto global.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| expressão | `string` | Expressão a ser avaliada. |  
| silent \(optional\) | `boolean` | No modo silencioso, as exceções lançadas durante a avaliação não são relatadas e não pausam a execução.  Substitui o `setPauseOnException` estado. |  
| contextId \(optional\) | [ExecutionContextId](#executioncontextid) | Especifica em qual contexto de execução executar a avaliação.  Se o parâmetro for omitido, a avaliação será executada no contexto da página inspecionada. |  
| returnByValue \(optional\) | `boolean` | Se o resultado é esperado para ser um objeto JSON que deve ser enviado por valor. |  
| awaitPromise \(optional\) | `boolean` | Se a execução `await` deve para o valor resultante e retornar uma vez que a promessa esperada for resolvida. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Resultado da avaliação. |  

---  

### <a name="callfunctionon"></a>callFunctionOn  

Função Calls com determinada declaração no objeto determinado.  O grupo de objetos do resultado é herdado do objeto de destino.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| functionDeclaration | `string` | Declaração da função a ser chamada. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificador da função de chamada do objeto.  Ou `objectId` `executionContextId` deve ser especificado.  objectId deve ser da função Runtime.evaluate(). |  
| argumentos \(optional\) | [CallArgument[]](#callargument) | Argumentos de chamada.  Todos os argumentos de chamada devem pertencer ao mesmo mundo JavaScript que o objeto de destino. |  
| silent \(optional\) | `boolean` | No modo silencioso, as exceções lançadas durante a avaliação não são relatadas e não pausam a execução.  Substitui o `setPauseOnException` estado. |  
| returnByValue \(optional\) | `boolean` | Se o resultado é esperado para ser um objeto JSON que deve ser enviado por valor. |  
| awaitPromise \(optional\) | `boolean` | Se a execução `await` deve para o valor resultante e retornar uma vez que a promessa esperada for resolvida. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Resultado da chamada. |  

---  

### <a name="getproperties"></a>getProperties  

Retorna propriedades de um determinado objeto.  O grupo de objetos do resultado é herdado do objeto de destino.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Identificador do objeto para o que retornar propriedades.  `objectId` deve ser da `Debugger.evaluateOnCallFrame()` função. |  
| ownProperties \(optional\) | `boolean` | Se `true` , retorna propriedades pertencentes apenas ao elemento em si, não à cadeia de protótipos. |  
| accessorPropertiesOnly \(optional\) | `boolean` | **Experimental**.  Se `true` , retorna propriedades do acessador \(somente com getter/setter\) ; as propriedades internas também não são retornadas. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| result | [PropertyDescriptor[]](#propertydescriptor) | Propriedades do objeto. |  

---  

## <a name="events"></a>Eventos  

### <a name="executioncontextscleared"></a>executionContextsCleared  

Emitido quando todos os executionContexts foram limpos no navegador.  

&nbsp;  

---  

### <a name="exceptionthrown"></a>exceptionThrown  

Emitido quando a exceção foi lançada e não foi acionada.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| timestamp | [Carimbo de data/hora](#timestamp) | Timestamp da exceção. |  
| exceptionDetails | [ExceptionDetails](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a>Tipos  

### <a name="scriptid-string"></a>Cadeia de caracteres ScriptId  

<a name="scriptid"></a>  

Identificador de script exclusivo.  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a>Cadeia de caracteres RemoteObjectId  

<a name="remoteobjectid"></a>  

Identificador de objeto exclusivo.  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a>Cadeia de caracteres UnserializableValue  

<a name="unserializablevalue"></a>  

Valor primitivo que não pode ser stringified JSON.  

##### <a name="allowed-values"></a>Valores permitidos  

`Infinity`, `NaN`, `-Infinity`, `-0`  

---  

### <a name="remoteobject-object"></a>Objeto RemoteObject  

<a name="remoteobject"></a>  

Objeto Mirror fazendo referência ao objeto JavaScript original.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| tipo | `string` | Tipo de objeto.  Valores permitidos:  `object` , , , , , `function` `undefined` `string` `number` `boolean` e `symbol` |  
| subtipo \(optional\) | `string` | Dica de subtipo de objeto.  Especificado apenas para `object` valores de tipo.  Valores permitidos:  `null` `error` , e `promise` |  
| className \(optional\) | `string` | Nome da classe de objeto \(construtor\).  Especificado apenas para `object` valores de tipo. |  
| valor \(opcional\) | `any` | Valor do objeto remoto em caso de valores primitivos ou valores JSON \(se foi solicitado\). |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | O valor primitivo que não pode ser stringified JSON não tem `value` , mas obtém essa propriedade. |  
| description \(optional\) | `string` | Representação de cadeia de caracteres do objeto. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificador de objeto exclusivo \(para valores não primitivos\). |  
| msDebuggerPropertyId \(optional\) | `string` | **Experimental**.  Microsoft: A ID da propriedade depurador associada para este objeto. |  

---  

### <a name="propertydescriptor-object"></a>Objeto PropertyDescriptor  

<a name="propertydescriptor"></a>  

Descritor da propriedade Object.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| name | `string` | Nome da propriedade ou descrição de símbolo. |  
| valor \(opcional\) | [RemoteObject](#remoteobject) | O valor associado à propriedade. |  
| writable \(optional\) | `boolean` | `True` se o valor associado à propriedade pode ser alterado \(descritores de dados somente\). |  
| get \(optional\) | [RemoteObject](#remoteobject) | Uma função que serve como um getter para a propriedade ou se não houver getter \(descritores do acessador `undefined` somente\). |  
| set \(optional\) | [RemoteObject](#remoteobject) | Uma função que serve como um setter para a propriedade ou se não houver setter \(descritores do acessador `undefined` somente\). |  
| configurável | `boolean` | `True` se o tipo desse descritor de propriedade pode ser alterado e se a propriedade pode ser excluída do objeto correspondente. |  
| enumerable | `boolean` | `True` se essa propriedade aparecer durante a enumeração das propriedades no objeto correspondente. |  
| wasThrown \(optional\) | `boolean` | `True` se o resultado foi lançado durante a avaliação. |  
| isOwn \(optional\) | `boolean` | `True` se a propriedade pertence ao objeto. |  
| msReturnValue \(optional\) | `boolean` | **Experimental**.  Microsoft:  `True` se a propriedade for um valor de retorno. |  
| símbolo \(opcional\) | [RemoteObject](#remoteobject) | Objeto símbolo de propriedade, se a propriedade for do `symbol` tipo. |  

---  

### <a name="callargument-object"></a>Objeto CallArgument  

<a name="callargument"></a>  

Representa o argumento de chamada de função.  A ID do objeto remoto , o valor primitivo `value` inserializável ou nenhum dos \(for undefined\) deve ser especificado.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| valor \(opcional\) | `any` | Valor primitivo ou objeto javascript serializable. |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | Valor primitivo que não pode ser stringified JSON. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificador de objeto remoto. |  

---  

### <a name="executioncontextid-integer"></a>ExecutionContextId integer  

<a name="executioncontextid"></a>  

ID de um contexto de execução.  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a>Objeto ExceptionDetails  

<a name="exceptiondetails"></a>  

Informações detalhadas sobre exceção \(ou error\) que foram lançadas durante a compilação ou execução do script.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| exceptionId | `integer` | ID de exceção. |  
| texto | `string` | Texto de exceção, que deve ser usado junto com o objeto exception quando disponível. |  
| lineNumber | `integer` | Número de linha do local de exceção \(0-based\). |  
| columnNumber | `integer` | Número da coluna do local de exceção \(0-based\). |  
| scriptId \(optional\) | [ScriptId](#scriptid) | ID do script do local de exceção. |  
| url \(optional\) | `string` | URL do local de exceção, a ser usada quando o script não foi relatado. |  
| stackTrace \(optional\) | [StackTrace](#stacktrace) | Rastreamento de pilha JavaScript, se disponível. |  
| exception \(optional\) | [RemoteObject](#remoteobject) | Objeto Exception, se disponível. |  
| executionContextId \(optional\) | [ExecutionContextId](#executioncontextid) | Identificador do contexto em que a exceção aconteceu. |  

---  

### <a name="timestamp-integer"></a>Número inteiro do timestamp  

<a name="timestamp"></a>  

Número de milissegundos desde a época.  

&nbsp;  

---  

### <a name="callframe-object"></a>Objeto CallFrame  

<a name="callframe"></a>  

Entrada de pilha para erros e declarações de tempo de execução.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| functionName | `string` | Nome da função JavaScript. |  
| scriptId | [ScriptId](#scriptid) | ID de script JavaScript. |  
| url | `string` | Nome ou url do script JavaScript. |  
| lineNumber | `integer` | Número da linha de script JavaScript \(0-based\). |  
| columnNumber | `integer` | Número da coluna de script JavaScript \(0-based\). |  

---  

### <a name="stacktrace-object"></a>Objeto StackTrace  

<a name="stacktrace"></a>  

Quadros de chamada para declarações ou mensagens de erro.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| description \(optional\) | `string` | Rótulo de cadeia de caracteres desse rastreamento de pilha.  Para rastreamentos assíncrono, pode ser um nome da função que iniciou a chamada assíncrona. |  
| callFrames | [CallFrame[]](#callframe) | Nome da função JavaScript. |  
| pai \(opcional\) | [StackTrace](#stacktrace) | Rastreamento de pilha JavaScript assíncrono que precedeu essa pilha, se disponível. |  

---  
