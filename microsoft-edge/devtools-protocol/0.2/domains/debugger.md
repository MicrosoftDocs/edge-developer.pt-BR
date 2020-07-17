---
description: Referência para o domínio do depurador. O domínio do depurador expõe recursos de depuração JavaScript. Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.
title: Debugger Domain-DevTools Protocol versão 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 3dae7e569db31cf2cff3cbb6d2a83cbead7ba22c
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882685"
---
# Debugger Domain-DevTools Protocol versão 0,2 (EdgeHTML)  

O domínio do depurador expõe recursos de depuração JavaScript. Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.

| | |
|-|-|
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [SetBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [StepOut](#stepout), [Pause](#pause), [resume](#resume), [getscriptname](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setvariablevalue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |
| [**Eventos**](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [pausado](#paused), [retomado](#resumed) |
| [**Tipos**](#types) | [Breakpointid](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope) |
| [**Dependências**](#dependencies) | [Tempo de Execução](runtime.md) |
## Métodos

### Habilitar
Habilita o depurador para a página especificada. Os clientes não devem presumir que a depuração foi habilitada até que o resultado desse comando seja recebido.

</p>

---

### Desabilitar 
Desabilita o depurador para determinada página.

</p>

---

### getPossibleBreakpoints
Retorna possíveis locais para o ponto de interrupção. os scripts em locais de intervalo de início e término devem ser iguais.

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
            <td>start</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Início do intervalo para pesquisar possíveis locais de ponto de interrupção em.</td>
        </tr>
        <tr>
            <td>encerrar</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Fim do intervalo para pesquisar possíveis locais de ponto de interrupção (excluindo). Quando não especificado, o final dos scripts é usado como final do intervalo.</td>
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
            <td>localiza</td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td>Lista de possíveis locais de ponto de interrupção.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointsActive
Ativa/desativa todos os pontos de interrupção na página.

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
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Novo valor para o estado ativo dos pontos de interrupção.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointByUrl
Define o ponto de interrupção JavaScript em um determinado local especificado por URL ou Regex de URL. Depois que esse comando for emitido, todos os scripts analisados existentes terão pontos de interrupção resolvidos e retornados na <code>locations</code> propriedade. A análise de script correspondente resultará em eventos subsequentes <code>breakpointResolved</code> emitidos. Esse ponto de interrupção lógico permanecerá recarregamentos de página.

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
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número da linha para definir o ponto de interrupção em.</td>
        </tr>
        <tr>
            <td>url <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL dos recursos para definir o ponto de interrupção.</td>
        </tr>
        <tr>
            <td>urlRegex <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Padrão Regex para as URLs dos recursos para definir os pontos de interrupção. <code>url</code>Ou <code>urlRegex</code> deve ser especificado.</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Offset na linha para definir o ponto de interrupção.</td>
        </tr>
        <tr>
            <td>problema <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Expressão a ser usada como uma condição de ponto de interrupção. Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</td>
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
            <td>breakpointid</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>ID do ponto de interrupção criado para referência adicional.</td>
        </tr>
        <tr>
            <td>localiza</td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td>Lista de locais para os quais esse ponto de interrupção foi resolvido após adição.</td>
        </tr>
    </tbody>
</table>
</p>

---

### SetBreakpoint
Define o ponto de interrupção JavaScript em um determinado local.

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
            <td>ponto</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Local para definir o ponto de interrupção.</td>
        </tr>
        <tr>
            <td>problema <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Expressão a ser usada como uma condição de ponto de interrupção. Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</td>
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
            <td>breakpointid</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>ID do ponto de interrupção criado para referência adicional.</td>
        </tr>
        <tr>
            <td>actualLocation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Local em que este ponto de interrupção foi resolvido.</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeBreakpoint
Remove o ponto de interrupção JavaScript.

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
            <td>breakpointid</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### stepOver
Etapas sobre a instrução.

</p>

---

### stepInto
Etapas para a chamada de função.

</p>

---

### passo a passo
Etapas para sair da chamada de função.

</p>

---

### pause
Para a próxima instrução JavaScript.

</p>

---

### resume
Retoma a execução do JavaScript.

</p>

---

### getscriptname
Retorna a origem do script com ID especificado.

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
            <td>scriptid</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>ID do script para o qual obter a fonte.</td>
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
            <td>scriptização</td>
            <td><code class="flyout">string</code></td>
            <td>Fonte de script.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setPauseOnExceptions
Define o estado pausar exceções. Pode ser definido para interromper todas as exceções, exceções não capturadas ou nenhuma exceção. O estado de pausa inicial em exceções é <code>none</code> .

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
            <td>Estado</td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: None, unpercebeud, All</i></td>
            <td>Pausar no modo de exceções.</td>
        </tr>
    </tbody>
</table>
</p>

---

### evaluateOnCallFrame
Avalia a expressão em um determinado quadro de chamada.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Identificador de quadro de chamada para avaliação.</td>
        </tr>
        <tr>
            <td>Express</td>
            <td><code class="flyout">string</code></td>
            <td>Expressão a ser avaliada.</td>
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
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Wrapper do objeto para o resultado da avaliação.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setvariablevalue
Altera o valor da variável em um callframe. Escopos baseados em objeto não são compatíveis e devem ser modificados manualmente.

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
            <td>scopeNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>número baseado em 0 do escopo como foi listado na cadeia de escopos. Somente os tipos de escopo ' local ', ' fechamento ' e ' Catch ' são permitidos. Outros escopos podem ser manipulados manualmente.</td>
        </tr>
        <tr>
            <td>VariableName</td>
            <td><code class="flyout">string</code></td>
            <td>Nome da variável.</td>
        </tr>
        <tr>
            <td>newValue</td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td>Novo valor de variável.</td>
        </tr>
        <tr>
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>ID de callframe que mantém a variável.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBlackboxPatterns
<span><b>Experimentais. </b></span>Substituir os padrões de Blackbox anteriores pelos aprovados. Força o back-end a ignorar a depuração/pausa em scripts com URL correspondente a um dos padrões. O depurador tentará deixar o script do blackboxed executando ' Step in ' várias vezes, finalmente reclassificando para "Step Out" se não tiver êxito.

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
            <td>padrões</td>
            <td><code class="flyout">string[]</code></td>
            <td>Matriz de regexps que será usada para verificar a URL do script para o estado Blackbox.</td>
        </tr>
    </tbody>
</table>
</p>

---

### msSetDebuggerPropertyValue
<span><b>Experimentais. </b></span>Microsoft: define a Propriedade Debugger especificada para o valor especificado.

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
            <td>debuggerPropertyId</td>
            <td><code class="flyout">string</code></td>
            <td>Microsoft: a identificação da propriedade (por exemplo, msDebuggerPropertyId) a ser definida.</td>
        </tr>
        <tr>
            <td>newValue</td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### scriptParsed
Acionado quando o script é analisado. Esse evento também é disparado para todos os scripts conhecidos e não coletados, quando o depurador é ativado.

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
            <td>scriptid</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificador do script analisado.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL ou nome do script analisado (se houver).</td>
        </tr>
        <tr>
            <td>início</td>
            <td><code class="flyout">integer</code></td>
            <td>Deslocamento de linha do script dentro do recurso com a URL fornecida (para marcas de script).</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>O deslocamento da coluna do script dentro do recurso com a URL fornecida.</td>
        </tr>
        <tr>
            <td>Line</td>
            <td><code class="flyout">integer</code></td>
            <td>Última linha do script.</td>
        </tr>
        <tr>
            <td>Coluna de EndColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Comprimento da última linha do script.</td>
        </tr>
        <tr>
            <td>executionContextid</td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td>Especifica o contexto de criação de script.</td>
        </tr>
        <tr>
            <td>sourceMapURL <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL do mapa de origem associado ao script (se houver).</td>
        </tr>
        <tr>
            <td>das <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Experimentais. </b></span>Esse tamanho do script.</td>
        </tr>
        <tr>
            <td>msParentId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Experimentais. </b></span>Esta é a ID do documento pai.</td>
        </tr>
        <tr>
            <td>msMimeType <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Experimentais. </b></span>Esse é o tipo MIME.</td>
        </tr>
        <tr>
            <td>msIsDynamicCode <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Experimentais. </b></span>Isso indica se é um código dinâmico.</td>
        </tr>
        <tr>
            <td>msLongDocumentId <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Experimentais. </b></span>Esta é a ID do documento longo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### breakpointResolved
Disparado quando o ponto de interrupção é resolvido para um script e local reais.

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
            <td>breakpointid</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Identificador exclusivo de ponto de interrupção.</td>
        </tr>
        <tr>
            <td>ponto</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Local do ponto de interrupção real.</td>
        </tr>
        <tr>
            <td>msLength <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Experimentais. </b></span>Microsoft: comprimento do código (ou seja, número de caracteres) no local do ponto de interrupção.</td>
        </tr>
    </tbody>
</table>
</p>

---

### pausado
Acionado quando os depuradores violam um ponto de interrupção ou uma exceção.

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
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Pilha de chamadas no depurador interrompido.</td>
        </tr>
        <tr>
            <td>motivo</td>
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: Breakpoint, Step, Exception, Other, EventListener</i></td>
            <td>Motivo da pausa.</td>
        </tr>
        <tr>
            <td>data <br/> <i>opcional</i></td>
            <td><code class="flyout">object</code></td>
            <td>Objeto que contém propriedades auxiliares de quebra específicas.</td>
        </tr>
        <tr>
            <td>hitBreakpoints <br/> <i>opcional</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>IDs de pontos de interrupção de acesso</td>
        </tr>
        <tr>
            <td>asyncStackTrace <br/> <i>opcional</i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td>Rastreamento de pilha assíncrono JavaScript.</td>
        </tr>
    </tbody>
</table>
</p>

---

### retomado
Acionado quando o depurador retomar a execução.

</p>

---

## Tipos

### <a name="breakpointid"></a> Breakpointid `string`

Identificador de ponto de interrupção.

</p>

---

### <a name="callframeid"></a> CallFrameId `string`

Identificador de quadro de chamada.

</p>

---

### <a name="location"></a> Localização `object`

Local no código-fonte.

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
            <td>scriptid</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificador de script reportado no <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número da linha no script (baseado em 0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Número da coluna no script (baseado em 0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> BreakLocation `object`

Interrompa o local no código-fonte.

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
            <td>scriptid</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificador de script reportado no <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Número da linha no script (baseado em 0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Número da coluna no script (baseado em 0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</td>
        </tr>
        <tr>
            <td>tipo <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Valores permitidos: debuggerStatement, Call, Return.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> CallFrame `object`

Quadro de chamada JavaScript. Matriz de quadros de chamadas formam a pilha de chamadas.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Identificador de quadro de chamada. Esse identificador só é válido enquanto o depurador está pausado.</td>
        </tr>
        <tr>
            <td>função FunctionName</td>
            <td><code class="flyout">string</code></td>
            <td>Nome da função JavaScript chamada neste quadro de chamada.</td>
        </tr>
        <tr>
            <td>functionLocation <br/> <i>opcional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b>Experimentais. </b></span>Local no código-fonte.</td>
        </tr>
        <tr>
            <td>ponto</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Local no código-fonte.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Nome ou URL do script JavaScript.</td>
        </tr>
        <tr>
            <td>scopeChain</td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td>Cadeia de escopos para este quadro de chamada.</td>
        </tr>
        <tr>
            <td>deste</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> objeto para este quadro de chamada.</td>
        </tr>
        <tr>
            <td>returnValue <br/> <i>opcional</i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>O valor que está sendo retornado, se a função estiver em um ponto de retorno.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> Escopo `object`

Descrição do escopo.

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
            <td><code class="flyout">string</code> <br/> <i>Valores permitidos: global, local, com, fechamento, catch, Block, script, eval, Module, Return</i></td>
            <td>Tipo de escopo.</td>
        </tr>
        <tr>
            <td>object</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Objeto que representa o escopo. Para <code>global</code> e <code>with</code> escopos, ele representa o objeto real; para o restante dos escopos, é um objeto transitório artificial enumerando variáveis de escopo como suas propriedades.</td>
        </tr>
        <tr>
            <td>name <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td>startLocation <br/> <i>opcional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Local no código-fonte onde o escopo é iniciado</td>
        </tr>
        <tr>
            <td>EndLocation <br/> <i>opcional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Local no código-fonte em que termina o escopo</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dependências

[Tempo de Execução](runtime.md)
