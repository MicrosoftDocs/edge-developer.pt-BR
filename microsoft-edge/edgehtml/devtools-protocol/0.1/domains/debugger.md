---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio de Depurador.  O domínio depurador expõe os recursos de depuração do JavaScript.  Ele permite definir e remover pontos de interrupção, passar pela execução, explorar rastreamentos de pilha, etc.
title: Domínio de depurador - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d63408e23fd8912cf617bfefae2b991387b45a38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397675"
---
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a>Domínio de depurador - DevTools Protocol Versão 0.1 (EdgeHTML)  
  
O domínio depurador expõe os recursos de depuração do JavaScript.  Ele permite definir e remover pontos de interrupção, passar pela execução, explorar rastreamentos de pilha, etc.

| Classificação | Membros |  
|:--- |:--- |  
| [Métodos](#methods) | [enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |  
| [Eventos](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed) |  
| [Tipos](#types) | [BreakpointId,](#breakpointid) [CallFrameId,](#callframeid) [Location,](#location) [BreakLocation,](#breaklocation) [CallFrame,](#callframe) [Scope](#scope) |  
| [Dependências](#dependencies) | [Tempo de Execução](./runtime.md) |  

## <a name="methods"></a>Métodos  

### <a name="enable"></a>Habilitar  

Habilita o depurador para a página determinada.  Os clientes não devem presumir que a depuração foi habilitada até que o resultado desse comando seja recebido.  

&nbsp;  

---  

### <a name="disable"></a>Desabilitar   

Desabilita o depurador para determinada página.  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a>getPossibleBreakpoints  

Retorna possíveis locais para ponto de interrupção.  scriptId em locais de intervalo inicial e final deve ser o mesmo.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| start | [Location](#location) | Início do intervalo para pesquisar possíveis locais de ponto de interrupção em. |  
| encerrar | [Location](#location) | Fim do intervalo para pesquisar possíveis locais de ponto de interrupção em \(excludendo\).  Quando não especificado, o fim dos scripts é usado como fim do intervalo. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| locations | [BreakLocation](#breaklocation) | Lista dos possíveis locais de ponto de interrupção. |  

---  

### <a name="setbreakpointsactive"></a>setBreakpointsActive  

Ativa/desativa todos os pontos de interrupção na página.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| active | `boolean` | Novo valor para o estado ativo de pontos de interrupção. |  

---  

### <a name="setbreakpointbyurl"></a>setBreakpointByUrl  

Define o ponto de interrupção JavaScript em determinado local especificado por URL ou URL regex.  Depois que esse comando for emitido, todos os scripts analisados existentes terão pontos de interrupção resolvidos e retornados na `locations` propriedade.  A análise de scripts correspondentes posteriores resultará em eventos `breakpointResolved` subsequentes emitidos.  Esse ponto de interrupção lógico sobreviverá a recarregações de página.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| lineNumber | `integer` | Número da linha para definir ponto de interrupção em. |  
| url \(optional\) | `string` | URL dos recursos para definir o ponto de interrupção. |  
| urlRegex \(optional\) | `string` | Padrão regex para as URLs dos recursos para definir pontos de interrupção.  Ou `url` `urlRegex` deve ser especificado. |  
| columnNumber \(optional\) | `integer` | Deslocamento na linha para definir ponto de interrupção em. |  
| condição \(opcional\) | `string` | Expressão a ser usada como uma condição de ponto de interrupção.  Quando especificado, o depurador só será parar no ponto de interrupção se essa expressão for avaliada como true. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID do ponto de interrupção criado para referência posterior. |  
| locations | [Local[]](#location) | Lista dos locais em que esse ponto de interrupção foi resolvido após a adição. |  

---  

### <a name="setbreakpoint"></a>setBreakpoint  

Define o ponto de interrupção JavaScript em um determinado local.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| location | [Location](#location) | Local para definir o ponto de interrupção. |  
| condição \(opcional\) | `string` | Expressão a ser usada como uma condição de ponto de interrupção.  Quando especificado, o depurador só será parar no ponto de interrupção se essa expressão for avaliada como true. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID do ponto de interrupção criado para referência posterior. |  
| actualLocation | [Location](#location) | Local em que o ponto de interrupção foi resolvido. |  

---  

### <a name="removebreakpoint"></a>removeBreakpoint  

Remove o ponto de interrupção JavaScript.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a>stepOver  

Etapas sobre a instrução.  

&nbsp;  

---  

### <a name="stepinto"></a>stepInto  

Etapas na chamada de função.  

&nbsp;  

---  

### <a name="stepout"></a>stepOut  

Sai da chamada de função.  

&nbsp;  

---  

### <a name="pause"></a>pause  

Para na próxima instrução JavaScript.  

&nbsp;  

---  

### <a name="resume"></a>resume  

Retoma a execução do JavaScript.  

&nbsp;  

---  

### <a name="getscriptsource"></a>getScriptSource  

Retorna a origem do script com a ID determinada.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | ID do script para o que obter a origem. |  
| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| scriptSource | `string` | Origem do script. |  

---  

### <a name="setpauseonexceptions"></a>setPauseOnExceptions  

Define pausa no estado de exceções.  Pode ser definido para parar em todas as exceções, exceções não ativas ou nenhuma exceção.  A pausa inicial no estado de exceções é `none` .  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| state | `string` | Pause no modo de exceções.  Valores permitidos:  `none` `uncaught` , e `all` |  

---  

### <a name="evaluateoncallframe"></a>evaluateOnCallFrame  

Avalia a expressão em um determinado quadro de chamada.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Identificador de quadro de chamada a ser avaliada. |  
| expressão | `string` | Expressão a ser avaliada. |  
| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| result | [Runtime.RemoteObject](./runtime.md#remoteobject) | Wrapper do objeto para o resultado da avaliação. |  

---  

### <a name="setvariablevalue"></a>setVariableValue  

Altera o valor da variável em um callframe.  Os escopos baseados em objeto não têm suporte e devem ser transformados manualmente.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| scopeNumber | `integer` | Número baseado em 0 do escopo conforme listado na cadeia de escopo.  Somente `local` , e os tipos de escopo são `closure` `catch` permitidos.  Outros escopos podem ser manipulados manualmente. |  
| variableName | `string` | Nome da variável. |  
| newValue | [Runtime.CallArgument](./runtime.md#callargument) | Novo valor variável. |  
| callFrameId | [CallFrameId](#callframeid) | ID do callframe que contém variável. |  

---  

### <a name="setblackboxpatterns"></a>setBlackboxPatterns  

**Experimental**.  Substitua padrões de caixa preta anteriores por aqueles passados.  Força o back-end a ignorar a revisão/pausa em scripts com a URL correspondente a um dos padrões.  O depurador tentará deixar o script em caixa preta executando várias vezes, finalmente `step in` recorrendo `step out` se não tiver êxito.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| patterns | `string[]` | Matriz de regexps que será usada para verificar a URL do script para o estado de blackbox. |  

---  

### <a name="mssetdebuggerpropertyvalue"></a>msSetDebuggerPropertyValue  

**Experimental**.  Microsoft: define a propriedade depurador especificada como o valor especificado.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| debuggerPropertyId | `string` | Microsoft: A ID da propriedade \(ou seja, msDebuggerPropertyId\) a ser definida. |  
| newValue | `string` | &nbsp; |  

---  

## <a name="events"></a>Eventos  

### <a name="scriptparsed"></a>scriptParsed  

Disparado quando o script é analisado.  Esse evento também é acionado para todos os scripts conhecidos e não recolhidos ao habilitar o depurador.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificador do script analisado. |  
| url | `string` | URL ou nome do script analisado \(se tiver\). |  
| startLine | `integer` | Deslocamento de linha do script dentro do recurso com a URL determinada \(para marcas de script\). |  
| startColumn | `integer` | Deslocamento de coluna do script dentro do recurso com a URL determinada. |  
| endLine | `integer` | Última linha do script. |  
| endColumn | `integer` | Comprimento da última linha do script. |  
| executionContextId | [Runtime.ExecutionContextId](./runtime.md#executioncontextid) | Especifica o contexto de criação de script. |  
| sourceMapURL \(optional\) | `string` | URL do mapa de origem associado ao script (se for o caso). |  
| comprimento \(opcional\) | `integer` | **Experimental**.  Este comprimento do script. |  
| msParentId \(optional\) | `string` | **Experimental**.  Esta é a ID do documento pai. |  
| msMimeType \(optional\) | `string` | **Experimental**.  Esse é o tipo de mime. |  
| msIsDynamicCode \(optional\) | `boolean` | **Experimental**.  Isso indica se é um código dinâmico. |  
| msLongDocumentId \(optional\) | `integer` | **Experimental**.  Esta é a ID do documento longa. |  

---  

### <a name="breakpointresolved"></a>breakpointResolved  

Acionado quando o ponto de interrupção é resolvido para um script e local reais.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | Identificador exclusivo do ponto de interrupção. |  
| location | [Location](#location) | Local real do ponto de interrupção. |  
| msLength \(optional\) | `integer` | **Experimental**.  Microsoft: Comprimento do código \(ou seja, número de caracteres\) no local do ponto de interrupção. |  

---  

### <a name="paused"></a>pausado  

Acionado quando os depurador quebram para um ponto de interrupção ou exceção.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| callFrames | [CallFrame[]](#callframe) | Pilha de chamada em que o depurador parou. |  
| reason | `string` | Pause reason.  Valores permitidos:  `breakpoint` `step` , , `exception` e `other` |  
| data \(optional\) | `object` | Objeto que contém propriedades auxiliares específicas de quebra. |  
| hitBreakpoints \(optional\) | `string[]` | Hit breakpoints IDs |  

---  

### <a name="resumed"></a>retomada  

Acionado quando o depurador retoma a execução.  

&nbsp;  

---  

## <a name="types"></a>Tipos  

### <a name="breakpointid-string"></a>Cadeia de caracteres BreakpointId  

<a name="breakpointid"></a>  

Identificador de ponto de interrupção.  

&nbsp;  

---  

### <a name="callframeid-string"></a>Cadeia de caracteres CallFrameId  

<a name="callframeid"></a>  

Identificador de quadro de chamada.  

&nbsp;  

---  

### <a name="location-object"></a>Objeto Location  

<a name="location"></a>  

Local no código-fonte.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificador de script conforme relatado no `Debugger.scriptParsed` . |  
| lineNumber | `integer` | Número da linha no script \(0-based\). |  
| columnNumber \(optional\) | `integer` | Número da coluna no script \(0-based\). |  
| msLength | `integer` | Microsoft: Comprimento do código \(ou seja, número de caracteres\) neste quadro de chamada. |  

---  

### <a name="breaklocation-object"></a>Objeto BreakLocation  

<a name="breaklocation"></a>  

Local de quebra no código-fonte.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificador de script conforme relatado no `Debugger.scriptParsed` . |  
| lineNumber | `integer` | Número da linha no script \(0-based\). |  
| columnNumber \(optional\) | `integer` | Número da coluna no script \(0-based\). |  
| msLength | `integer` | Microsoft: Comprimento do código \(ou seja, número de caracteres\) neste quadro de chamada. |  
| tipo \(opcional\) | `string` | Valores permitidos:  `debuggerStatement` `call` , e `return` |  

---  

### <a name="callframe-object"></a>Objeto CallFrame  

<a name="callframe"></a>  

Quadro de chamada JavaScript.  Matriz de quadros de chamada forma a pilha de chamada.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Identificador de quadro de chamada.  Esse identificador só é válido enquanto o depurador é pausado. |  
| functionName | `string` | Nome da função JavaScript chamada neste quadro de chamada. |  
| functionLocation \(optional\) | [Location](#location) | **Experimental**.  Local no código-fonte. |  
| location | [Location](#location) | Local no código-fonte. |  
| url | `string` | Nome ou url do script JavaScript. |  
| scopeChain | [Scope[]](#scope) | Cadeia de escopo para esse quadro de chamada. |  
| this | [Runtime.RemoteObject](./runtime.md#remoteobject) | `this` para esse quadro de chamada. |  
| returnValue \(optional\) | [Runtime.RemoteObject](./runtime.md#remoteobject) | O valor que está sendo retornado, se a função estiver no ponto de retorno. |  

---  

### <a name="scope-object"></a>Objeto Scope  

<a name="scope"></a>  

Descrição do escopo.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| tipo | `string` | Tipo de escopo.  Valores permitidos:  `global` , , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` e `module` |  
| object | [Runtime.RemoteObject](./runtime.md#remoteobject) | Objeto que representa o escopo.  Para e escopos ele representa o objeto real; para o restante dos escopos, ele é `global` objeto transitório artificial enumerando variáveis de escopo `with` como suas propriedades. |  
| nome \(opcional\) | `string` | &nbsp; |  
| startLocation \(optional\) | [Location](#location) | Local no código-fonte onde o escopo é iniciado. |  
| endLocation \(optional\) | [Location](#location) | Local no código-fonte onde o escopo termina. |  

---  

## <a name="dependencies"></a>Dependências  

[Tempo de Execução](./runtime.md)  
