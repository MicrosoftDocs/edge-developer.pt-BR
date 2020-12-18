---
description: Referência do protocolo DevTools versão 0,2 (EdgeHTML) do domínio de tempo de execução. O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos. Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior. Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.
title: Domínio de tempo de execução-DevTools protocolo versão 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f18cca951b298e8b4d870a7d722f30c9d28ad346
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231685"
---
# Domínio de tempo de execução-DevTools protocolo versão 0,2 (EdgeHTML)  

O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos. Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior. Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.

| | |
|-|-|
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar](#disable), [avaliar](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseobject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries) |
| [**Eventos**](#events) | [executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled) |
| [**Tipos**](#types) | [Scriptid](#scriptid), [RemoteObjectId](#remoteobjectid), [unserializablevalue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [executioncontextid](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |
## Métodos

### Habilitar
Habilita o relatório dos <code>executionContextCreated</code> <code>executionContextDestroyed</code> eventos e <code>executionContextsCleared</code> . Quando o relatório é ativado <code>executionContextCreated</code> , o evento será enviado imediatamente para cada contexto de execução existente.

</p>

---

### Desabilitar 
Desabilita o relatório dos <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> eventos e.

</p>

---

### retornará
Avalia a expressão no objeto global.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Express</td>
            <td><code class="flyout">string</code></td>
            <td>Expressão a ser avaliada.</td>
        </tr>
        <tr>
            <td>includeCommandLineAPI <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Determina se a API de linha de comando deve estar disponível durante a avaliação.</td>
        </tr>
        <tr>
            <td>objeto de objeto <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nome do grupo simbólico que pode ser usado para liberar vários objetos.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução. Substitui o <code>setPauseOnException</code> estado.</td>
        </tr>
        <tr>
            <td>ContextId <br/> <i>opcional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Especifica em qual contexto de execução executar avaliação. Se o parâmetro for omitido, a avaliação será executada no contexto da página inspecionada.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devolver</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>levar</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Resultado da avaliação.</td>
        </tr>
    </tbody>
</table>
</p>

---

### callFunctionOn
Função calls com declaração fornecida no objeto especificado. O grupo de objetos do resultado é herdado do objeto de destino.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>functionDeclaration</td>
            <td><code class="flyout">string</code></td>
            <td>Declaração da função a ser chamada.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>opcional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador do objeto no qual a função deve ser chamada. O objectId ou o executionContextid deve ser especificado.  objectId deve ser da função Runtime. Evaluate ().</td>
        </tr>
        <tr>
            <td>arguments <br/> <i>opcional</i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td>Argumentos de chamada. Todos os argumentos de chamada devem pertencer ao mesmo mundo JavaScript que o objeto de destino.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução. Substitui o <code>setPauseOnException</code> estado.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</td>
        </tr>
        <tr>
            <td>executionContextid <br/> <i>opcional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Especifica o contexto de execução em que o objeto global será usado para chamar a função. O executionContextid ou o objectId deve ser especificado.</td>
        </tr>
        <tr>
            <td>objeto de objeto <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nome do grupo simbólico que pode ser usado para liberar vários objetos. Se o objeto de objeto não for especificado e objectId for, o objeto de objeto será herdado do objeto.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devolver</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>levar</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Resultado da chamada.</td>
        </tr>
    </tbody>
</table>
</p>

---

### awaitPromise
Adicione o manipulador a promessa com a ID de objeto Promise fornecida.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>promiseObjectId</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador da promessa.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devolver</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>levar</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Resultado da promessa.  Conterá o valor rejeitado se a promessa foi rejeitada.</td>
        </tr>
    </tbody>
</table>
</p>

---

### GetProperties
Retorna as propriedades de um determinado objeto. O grupo de objetos do resultado é herdado do objeto de destino.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>objectId</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador do objeto para o qual as propriedades são retornadas. objectId deve ser da função Debugger. evaluateOnCallFrame ().</td>
        </tr>
        <tr>
            <td>ownProperties <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se verdadeiro, retorna propriedades pertencentes somente ao elemento em si, não à sua cadeia de protótipos.</td>
        </tr>
        <tr>
            <td>accessorPropertiesOnly <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Experimentais. </b></span>Se verdadeiro, retorna propriedades de assessor (somente com getter/setter); as propriedades internas também não são retornadas.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devolver</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>levar</td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td>Propriedades do objeto.</td>
        </tr>
    </tbody>
</table>
</p>

---

### globalLexicalScopeNames
Retorna todas as variáveis Let, const e Class do escopo global do console.

<table>
    <thead>
        <tr>
            <th>Devolver</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>os</td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### releaseobject
Libera o objeto remoto com a ID especificada.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>objectId</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador do objeto a ser liberado. </td>
        </tr>
    </tbody>
</table>
</p>

---

### releaseObjectGroup
Libera todos os objetos remotos que pertencem a um determinado grupo.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>objeto de objeto</td>
            <td><code class="flyout">string</code></td>
            <td>Nome do grupo de objetos simbólico. </td>
        </tr>
    </tbody>
</table>
</p>

---

### discardConsoleEntries
Descarta exceções coletadas e chamadas de API do console.

</p>

---

## Eventos

### executionContextCreated
Emitido quando um novo contexto de execução é criado.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>atalho</td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td>Um contexto de execução recém criado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextDestroyed
Emitido quando o contexto de execução é destruído.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>executionContextid</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>ID do contexto destruído</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextsCleared
Emitido quando todos os executionContext foram limpos no navegador

</p>

---

### exceptionThrown
Emitido quando a exceção foi gerada e não tratada.

<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>carimbo</td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Carimbo de data/hora da exceção.</td>
        </tr>
        <tr>
            <td>exceptionDetails</td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### consoleAPICalled


<table>
    <thead>
        <tr>
            <th>Parâmetros</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>tipo</td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: log, info, aviso, erro, depuração, Assert, Table, Trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, timeStamp, Start, startGroupCollapsed, ENDGROUP</i></td>
            <td>Tipo de chamada. Isso inclui log, informações, Warn, erro, depuração, Assert, Table, Trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, Exception, timeStamp, Group, groupCollapsed, groupEnd.</td>
        </tr>
        <tr>
            <td>args</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td>Argumentos de chamada.</td>
        </tr>
        <tr>
            <td>executionContextid</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Identificador do contexto em que foi feita a chamada do console</td>
        </tr>
        <tr>
            <td>carimbo <br/> <i>opcional</i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Carimbo de data/hora da chamada.</td>
        </tr>
        <tr>
            <td>Pilha <br/> <i>opcional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Rastreamento de pilha capturado se disponível</td>
        </tr>
    </tbody>
</table>
</p>

---

## Tipos

### <a name="scriptid"></a> Scriptid `string`

Identificador de script exclusivo.

</p>

---

### <a name="remoteobjectid"></a> RemoteObjectId `string`

Identificador de objeto exclusivo.

</p>

---

### <a name="unserializablevalue"></a> Unserializablevalue `string`

Valor primitivo que não pode ser JSON-stringified.

##### Valores permitidos
Infinito, NaN,-Infinity,-0
</p>

---

### <a name="remoteobject"></a> RemoteObject `object`

Objeto espelho que faz referência ao objeto JavaScript original.

<table>
    <thead>
        <tr>
            <th>Propriedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>tipo</td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: Object, Function, undefined, String, Number, booliano, símbolo</i></td>
            <td>Tipo de objeto.</td>
        </tr>
        <tr>
            <td>subtipo <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: NULL, Error, Promise, Node</i></td>
            <td>Dica de subtipo de objeto. Especificado <code>object</code> apenas para valores de tipo.</td>
        </tr>
        <tr>
            <td>Classe <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nome do Construtor (classe objeto). Especificado <code>object</code> apenas para valores de tipo.</td>
        </tr>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><code class="flyout">any</code></td>
            <td>Valor do objeto remoto em caso de valores primitivos ou valores JSON (se for solicitado).</td>
        </tr>
        <tr>
            <td>unserializablevalue <br/> <i>opcional</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Um valor primitivo que não pode ser JSON-stringified não tem <code>value</code>, mas obtém essa propriedade.</td>
        </tr>
        <tr>
            <td>description <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Representação de cadeia de caracteres do objeto.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>opcional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador de objeto exclusivo (para valores não primitivos).</td>
        </tr>
        <tr>
            <td>msDebuggerPropertyId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Experimentais. </b></span>Microsoft: a ID de Propriedade do depurador associado a esse objeto.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> PropertyDescriptor `object`

Descritor de propriedades do objeto.

<table>
    <thead>
        <tr>
            <th>Propriedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nome da propriedade ou descrição do símbolo.</td>
        </tr>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>O valor associado à propriedade.</td>
        </tr>
        <tr>
            <td>gravável <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Verdadeiro se o valor associado à propriedade pode ser alterado (somente descritores de dados).</td>
        </tr>
        <tr>
            <td>obter <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Uma função que serve como um getter para a propriedade, ou <code>undefined</code> se não houver nenhum getter (somente descritores de acessador).</td>
        </tr>
        <tr>
            <td>set <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Uma função que serve como um setter para a propriedade ou <code>undefined</code> se não houver nenhum setter (somente descritores de acesso).</td>
        </tr>
        <tr>
            <td>configurável</td>
            <td><code class="flyout">boolean</code></td>
            <td>True se o tipo desse descritor de propriedades pode ser alterado e se a propriedade pode ser excluída do objeto correspondente.</td>
        </tr>
        <tr>
            <td>enumer</td>
            <td><code class="flyout">boolean</code></td>
            <td>Verdadeiro se essa propriedade aparecer durante a enumeração das propriedades no objeto correspondente.</td>
        </tr>
        <tr>
            <td>wasThrown <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Verdadeiro se o resultado foi lançado durante a avaliação.</td>
        </tr>
        <tr>
            <td>isOwn <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Verdadeiro se a propriedade for proprietária para o objeto.</td>
        </tr>
        <tr>
            <td>msReturnValue <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Experimentais. </b></span>Microsoft: true se a propriedade for um valor de retorno.</td>
        </tr>
        <tr>
            <td>symbol <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Objeto de símbolo de propriedade, se a propriedade for do `symbol` tipo. </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> CallArgument `object`

Representa o argumento de chamada de função. A ID de objeto remoto <code>objectId</code> , primitiva <code>value</code> , valor primitivo não serializável ou nenhum dos (para Undefined) eles devem ser especificados.

<table>
    <thead>
        <tr>
            <th>Propriedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><code class="flyout">any</code></td>
            <td>Valor primitivo ou objeto JavaScript serializável.</td>
        </tr>
        <tr>
            <td>unserializablevalue <br/> <i>opcional</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Valor primitivo que não pode ser JSON-stringified.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>opcional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificador de objeto remoto.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> ExecutionContextid `integer`

ID de um contexto de execução.

</p>

---

### <a name="executioncontextdescription"></a> ExecutionContextDescription `object`

Descrição de um mundo isolado.

<table>
    <thead>
        <tr>
            <th>Propriedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>id</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>ID exclusiva do contexto de execução. Ele pode ser usado para especificar em qual execução a avaliação de script de contexto deve ser realizada.</td>
        </tr>
        <tr>
            <td>Origin</td>
            <td><code class="flyout">string</code></td>
            <td>Origem do contexto de execução.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nome legível pelo homem descrevendo o contexto determinado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> ExceptionDetails `object`

Informações detalhadas sobre exceção (ou erro) que foi lançada durante a compilação ou execução de scripts.

<table>
    <thead>
        <tr>
            <th>Propriedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>exceptionid</td>
            <td><code class="flyout">integer</code></td>
            <td>ID da exceção.</td>
        </tr>
        <tr>
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Texto de exceção, que deve ser usado em conjunto com o objeto de exceção quando disponível.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número da linha do local da exceção (com base em 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número da coluna do local da exceção (com base em 0).</td>
        </tr>
        <tr>
            <td>scriptid <br/> <i>opcional</i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>ID do script do local da exceção.</td>
        </tr>
        <tr>
            <td>url <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL do local da exceção, a ser usado quando o script não foi reportado.</td>
        </tr>
        <tr>
            <td>Pilha <br/> <i>opcional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Rastreamento de pilha JavaScript, se disponível.</td>
        </tr>
        <tr>
            <td>extremamente <br/> <i>opcional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Objeto de exceção, se disponível.</td>
        </tr>
        <tr>
            <td>executionContextid <br/> <i>opcional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Identificador do contexto em que ocorreu a exceção.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> Carimbo de data/hora `integer`

Número de milissegundos desde a época.

</p>

---

### <a name="callframe"></a> CallFrame `object`

Entrada de pilha para erros e asserções de tempo de execução.

<table>
    <thead>
        <tr>
            <th>Propriedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>função FunctionName</td>
            <td><code class="flyout">string</code></td>
            <td>Nome da função JavaScript.</td>
        </tr>
        <tr>
            <td>scriptid</td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>Identificação do script JavaScript. O scriptid estará vazio se o depurador não estiver habilitado.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Nome ou URL do script JavaScript.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número da linha de script JavaScript (com base em 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número da coluna de script JavaScript (baseado em 0).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> Pilha `object`

Quadros de chamadas para asserções ou mensagens de erro.

<table>
    <thead>
        <tr>
            <th>Propriedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>description <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Rótulo de cadeia de caracteres deste rastreamento de pilha. Para rastreamentos assíncronos, pode ser um nome da função que iniciou a chamada assíncrona.</td>
        </tr>
        <tr>
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Nome da função JavaScript.</td>
        </tr>
        <tr>
            <td>mãe <br/> <i>opcional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Rastreamento de pilha JavaScript assíncrono que precede esta pilha, se disponível.</td>
        </tr>
    </tbody>
</table>
</p>

---
