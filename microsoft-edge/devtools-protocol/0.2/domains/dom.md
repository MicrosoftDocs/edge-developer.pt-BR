---
description: Referência para o domínio DOM. Esse domínio apresenta operações DOM de leitura/gravação. Cada nó DOM é representado com seu objeto espelho que tem um `id` . Isso `id` pode ser usado para obter informações adicionais sobre o nó, solucioná-lo para o invólucro do objeto JavaScript, etc. É importante que o cliente receba eventos DOM somente para os nós conhecidos do cliente. O back-end mantém o controle dos nós que foram enviados para o cliente e nunca envia o mesmo nó duas vezes. É responsabilidade do cliente coletar informações sobre os nós que foram enviados ao cliente.<p>Observe que `iframe` os elementos Owner retornarão elementos de documento correspondentes como seus nós filho.</p>
title: DOM Domain – protocolo DevTools versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 9ebe5ff709ac2981cb2359b7279c5d4e5d375426
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561338"
---
# DOM
Esse domínio apresenta operações DOM de leitura/gravação. Cada nó DOM é representado com seu objeto espelho que tem um `id` . Isso `id` pode ser usado para obter informações adicionais sobre o nó, solucioná-lo para o invólucro do objeto JavaScript, etc. É importante que o cliente receba eventos DOM somente para os nós conhecidos do cliente. O back-end mantém o controle dos nós que foram enviados para o cliente e nunca envia o mesmo nó duas vezes. É responsabilidade do cliente coletar informações sobre os nós que foram enviados ao cliente.<p>Observe que `iframe` os elementos Owner retornarão elementos de documento correspondentes como seus nós filho.</p>

| | |
|-|-|
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar](#disable), [GetDocument](#getdocument), [HighlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [GetAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode) |
| [**Eventos**](#events) | [setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated) |
| [**Tipos**](#types) | [RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [node](#node), [BackendNodeId](#backendnodeid), [pseudotype](#pseudotype) |
| [**Dependências**](#dependencies) | [Classpath](runtime.md) |
## Métodos

### Habilitar
Habilita o agente DOM para a página especificada.

</p>

---

### Desabilitar 
Desabilita o agente DOM para a página especificada. Desabilitar o DOM invalidará qualquer nodeIds válido anteriormente.

</p>

---

### GetDocument
Retorna o nó DOM raiz (e, opcionalmente, a subárvore) para o chamador. A chamada `getDocument` invalidará qualquer nodeIds válido anteriormente

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
            <td>profundo</td>
            <td><code class="flyout">integer</code></td>
            <td>A profundidade máxima na qual os filhos devem ser recuperados, o padrão é 2. Use-1 para subárvore inteira.</td>
        </tr>
        <tr>
            <td>Pierce</td>
            <td><code class="flyout">boolean</code></td>
            <td>Se os iframes devem ou não ser percorridos ao retornar a subárvore (o padrão é falso).</td>
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
            <td>raiz</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Nó resultante.</td>
        </tr>
    </tbody>
</table>
</p>

---

### highlightNode
Nó DOM higlights com ID ou wrapper de objeto especificado. NodeId, backendNodeId ou objectId deve ser especificado.

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
            <td>NodeId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador do nó a ser realçado.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>opcional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Identificador do nó back-end a ser realçado.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>opcional</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>ID do objeto JavaScript do nó a ser realçado.</td>
        </tr>
        <tr>
            <td>higlightConfig</td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td>Descritor da aparência do realce.</td>
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
            <td>raiz</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Nó resultante.</td>
        </tr>
    </tbody>
</table>
</p>

---

### hideHighlight
Oculta qualquer realce do nó DOM atual.

</p>

---

### requestChildNodes
Solicitações que os filhos do nó com ID fornecida são retornadas para o chamador Ghe na forma de `setChildNodes` eventos. `setChildNodes` será disparado para cada nó que não tenha sido retornado anteriormente, a partir do nó solicitado até a profundidade especificada.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó do qual obter filhos.</td>
        </tr>
        <tr>
            <td>profundo</td>
            <td><code class="flyout">integer</code></td>
            <td>A profundidade máxima na qual os filhos devem ser recuperados, o padrão é 1. Use-1 para subárvore inteira.</td>
        </tr>
        <tr>
            <td>Pierce</td>
            <td><code class="flyout">boolean</code></td>
            <td>Se os iframes devem ou não ser percorridos ao retornar a subárvore (o padrão é falso).</td>
        </tr>
    </tbody>
</table>
</p>

---

### GetAttributes
Retorna atributos para o nó especificado.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó para o qual recuperar o attibutes.</td>
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
            <td>Attribute</td>
            <td><code class="flyout">string[]</code></td>
            <td>Uma matriz entrelaçada de nomes e valores de atributo de nó.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getOuterHTML
Retorna a marcação HTML do nó.

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
            <td>NodeId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador do nó.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>opcional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Identificador do nó back-end.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>opcional</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>ID de objeto JavaScript do invólucro de nó.</td>
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
            <td>outerHTML</td>
            <td><code class="flyout">string</code></td>
            <td>Marcação HTML externa.</td>
        </tr>
    </tbody>
</table>
</p>

---

### pushNodesByBackendIdsToFrontend
Procura IDs de nó e resolve todos os pais para as IDs de nó de back-end especificadas

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
            <td>backendNodeIds</td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td>IDs de nó de back-end dos nós a serem resolvidos</td>
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
            <td>nodeIds</td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>IDs de nó dos nós resolvidos</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelector
Executa `querySelector` em um determinado nó.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó para consulta.</td>
        </tr>
        <tr>
            <td>seletor</td>
            <td><code class="flyout">string</code></td>
            <td>A cadeia de caracteres do seletor.</td>
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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Resultado do seletor de consulta.</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelectorAll
Executa `querySelectorAll` em um determinado nó.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó para consulta.</td>
        </tr>
        <tr>
            <td>seletor</td>
            <td><code class="flyout">string</code></td>
            <td>A cadeia de caracteres do seletor.</td>
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
            <td>nodeIds</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Resultados do seletor de consulta.</td>
        </tr>
    </tbody>
</table>
</p>

---

### requestNode
Solicita que o nó com a ID de objeto remoto fornecido seja enviado ao chamador. Todos os nós que formam o caminho do nó para a raiz também são enviados ao cliente como uma série de `setChildNodes` notificações. Retorna 0 se o documento que contém o nó solicitado não tiver sido solicitado anteriormente pelo cliente.

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
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>ID do objeto JavaScript para converter em nó.</td>
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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó para determinado objeto.</td>
        </tr>
    </tbody>
</table>
</p>

---

### resolveNode
Resolve o objeto de nó JavaScript para um determinado NodeId ou BackendNodeId.

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
            <td>NodeId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó a ser resolvido.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>opcional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>ID do nó back-end do nó a ser resolvido.</td>
        </tr>
        <tr>
            <td>objeto de objeto</td>
            <td><code class="flyout">string</code></td>
            <td>Nome do grupo simbólico que pode ser usado para liberar vários objetos.</td>
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
            <td>object</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Wrapper do objeto JavaScript para o nó fornecido.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setInspectedNode
<span><b>Experimentais. </b></span>Permite que o console se refira ao nó inspecionado anterior com uma determinada ID via $0-$ 4.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó DOM para ser acessível por meio de $0-$ 4 na API da linha de comando.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### setChildNodes
Disparado quando o back-end deseja fornecer ao cliente a estrutura DOM ausente. Isso acontece na maioria das chamadas solicitando nodeIds

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
            <td>parentId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Nó pai para poplate com filhos.</td>
        </tr>
        <tr>
            <td>Nós</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Matriz de nós filho.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeModified
Disparado quando o `Element` atributo for modificado.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó que foi alterado.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nome do atributo.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valor do atributo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeRemoved
Disparado quando o `Element` atributo for removido.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó que foi alterado.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nome do atributo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### characterDataModified
Evento de espelhos `DOMCharacterDataModified` .

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó que foi alterado.</td>
        </tr>
        <tr>
            <td>charcterData</td>
            <td><code class="flyout">string</code></td>
            <td>Novo valor de texto.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeInserted
Evento de espelhos `DOMNodeInserted` .

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó que foi alterado.</td>
        </tr>
        <tr>
            <td>previousNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do irmão anterior do nó inserido.</td>
        </tr>
        <tr>
            <td>nó</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Dados de nó inseridos.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeRemoved
Evento de espelhos `DOMNodeRemoved` .

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó que foi alterado.</td>
        </tr>
        <tr>
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID do nó que foi removido.</td>
        </tr>
    </tbody>
</table>
</p>

---

### documentUpdated
Acionado quando foi `Document` totalmente atualizado. As IDs de nó não são mais válidas.

</p>

---

## Tipos

### <a name="rgba"></a> RGBA `object`

Uma estrutura que contém uma cor RGBA.

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
            <td>r</td>
            <td><code class="flyout">integer</code></td>
            <td>O componente vermelho, no intervalo [0-255].</td>
        </tr>
        <tr>
            <td>p</td>
            <td><code class="flyout">integer</code></td>
            <td>O componente verde, no intervalo [0-255].</td>
        </tr>
        <tr>
            <td>b</td>
            <td><code class="flyout">integer</code></td>
            <td>O componente azul, no intervalo [0-255].</td>
        </tr>
        <tr>
            <td>a <br/> <i>opcional</i></td>
            <td><code class="flyout">number</code></td>
            <td>O componente alfa, no intervalo [0-1]. O padrão é 1.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> HighlightConfig `object`

Dados de configuração para realce de elementos de página.

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
            <td>contentColor <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>A caixa de conteúdo realçar cor de preenchimento. O padrão é transparente.</td>
        </tr>
        <tr>
            <td>paddingColor <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>A cor de preenchimento da realce de preenchimento. O padrão é transparente.</td>
        </tr>
        <tr>
            <td>CorDaBorda <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>A borda realce cor de preenchimento. O padrão é transparente.</td>
        </tr>
        <tr>
            <td>marginColor <br/> <i>opcional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>A cor de preenchimento da margem de realce. O padrão é transparente.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> NodeId `integer`

Identificador de nó DOM exclusivo

</p>

---

### <a name="node"></a> Nó `object`

Objeto espelho que representa os nós DOM reais.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador de nó usado para fazer referência a esse nó. O backend irá disparar eventos DOM para nós que têm um NodeId conhecido para o cliente</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>opcional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador de nó do nó pai, se houver.</td>
        </tr>
        <tr>
            <td>backendNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificador de nó de back-end do nó. BackendNodeIds nós de referência que podem ser conhecidos pelo cliente, mas não enviem eventos DOM sobre esse nó.</td>
        </tr>
        <tr>
            <td>nodeType</td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`nodeType do.</td>
        </tr>
        <tr>
            <td>Node</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`NodeName.</td>
        </tr>
        <tr>
            <td>localName</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`localName do</td>
        </tr>
        <tr>
            <td>NodeValue</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`NodeValue</td>
        </tr>
        <tr>
            <td>childNodeCount <br/> <i>opcional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Contagem filho para `Container` nós.</td>
        </tr>
        <tr>
            <td>menores de idade <br/> <i>opcional</i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Nós filho deste nó quando solicitado com filhos.</td>
        </tr>
        <tr>
            <td>Attribute <br/> <i>opcional</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Atributos de `Element` nós na forma de uma matriz plana ' [Nome1, valor1, Nome2, valor2]</td>
        </tr>
        <tr>
            <td>documentURL <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL do documento para o qual os `Document` nós apontam.</td>
        </tr>
        <tr>
            <td>baseURL <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL do documento `Document` usada pelos nós para completar a URL.</td>
        </tr>
        <tr>
            <td>PublicId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` PublicId do nó.</td>
        </tr>
        <tr>
            <td>SystemId <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` SystemId do nó.</td>
        </tr>
        <tr>
            <td>internalSubset <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` InternalSubset do nó.</td>
        </tr>
        <tr>
            <td>xmlversão <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` A versão do nó XML no caso de documentos XML.</td>
        </tr>
        <tr>
            <td>name <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Nome do nó.</td>
        </tr>
        <tr>
            <td>value <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Valor do nó.</td>
        </tr>
        <tr>
            <td>frameid <br/> <i>opcional</i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td>ID do quadro para elementos de proprietário do quadro.</td>
        </tr>
        <tr>
            <td>contentDocument <br/> <i>opcional</i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Documento de conteúdo para elementos de proprietário do quadro.</td>
        </tr>
        <tr>
            <td>isSVG <br/> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Verdadeiro se o nó for SVG.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> BackendNodeId `integer`

Identificador de nó DOM exclusivo usado para fazer referência a um nó que pode não ter sido enviado para o front-end.

</p>

---

### <a name="pseudotype"></a> Pseudotype `string`

Pseudo-tipo de elemento.

##### Valores permitidos
primeira linha, primeira letra, antes, depois, seleção
</p>

---

## Dependências

[Classpath](runtime.md)