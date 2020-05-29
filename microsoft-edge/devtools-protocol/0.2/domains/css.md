---
description: Referência para o domínio CSS. Esse domínio expõe operações CSS de leitura/gravação. Todos os objetos CSS (folhas de estilo, regras e estilos) têm um associado `id` usado em operações subsequentes no objeto relacionado. Cada tipo de objeto tem uma `id` estrutura específica, e não é intercambiável entre objetos de tipos diferentes. Objetos CSS podem ser carregados usando-se as `get*ForNode()` chamadas (que aceitam uma ID de nó DOM). Um cliente também pode controlar as folhas de estilo por meio dos `styleSheetAdded` / `styleSheetRemoved` eventos e carregar subseqüentemente o conteúdo da folha de estilos usando os `getStyleSheet[Text]()` métodos.
title: Protocolo CSS Domain-DevTools versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 939eda0ae2f5228657d35899ab75b39493eff917
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561344"
---
# CSS
Esse domínio expõe operações CSS de leitura/gravação. Todos os objetos CSS (folhas de estilo, regras e estilos) têm um associado `id` usado em operações subsequentes no objeto relacionado. Cada tipo de objeto tem uma `id` estrutura específica, e não é intercambiável entre objetos de tipos diferentes. Objetos CSS podem ser carregados usando-se as `get*ForNode()` chamadas (que aceitam uma ID de nó DOM). Um cliente também pode controlar as folhas de estilo por meio dos `styleSheetAdded` / `styleSheetRemoved` eventos e carregar subseqüentemente o conteúdo da folha de estilos usando os `getStyleSheet[Text]()` métodos.

| | |
|-|-|
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode) |
| [**Eventos**](#events) | [styleSheetAdded](#stylesheetadded), [stylesheetchanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved) |
| [**Tipos**](#types) | [Stylesheetid](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [selectorlist](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader) |
| [**Dependências**](#dependencies) | [DOM](dom.md) |
## Métodos

### Habilitar
Habilita o agente CSS para a página especificada. Os clientes não devem presumir que o agente de CSS foi habilitado até que o resultado desse comando seja recebido.

</p>

---

### Desabilitar 
Desabilita o agente CSS para a página especificada.

</p>

---

### getInlineStylesForNode
Retorna os estilos embutidos definidos (explicitamente no atributo "Style" e implicitamente, usando atributos DOM) para um nó DOM identificado por `nodeId` .

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
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
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
            <td>inlinestyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo embutido para o nó DOM especificado.</td>
        </tr>
        <tr>
            <td>attributestyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo de elemento definido pelo atributo (por exemplo, resultante de "width = 20 Height = 100%").</td>
        </tr>
    </tbody>
</table>
</p>

---

### getMatchedStylesForNode
Retorna os estilos solicitados para um nó DOM identificado por `nodeId` .

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
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
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
            <td>inlinestyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo embutido para o nó DOM especificado.</td>
        </tr>
        <tr>
            <td>attributestyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo de elemento definido pelo atributo (por exemplo, resultante de "width = 20 Height = 100%").</td>
        </tr>
        <tr>
            <td>matchedCSSRules <br /> <i>opcional</i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Regras CSS correspondentes a esse nó, de todas as folhas de estilo aplicáveis.</td>
        </tr>
        <tr>
            <td>pseudoElements <br /> <i>opcional</i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td>O pseudo estilo corresponde a este nó.</td>
        </tr>
        <tr>
            <td>substituir <br /> <i>opcional</i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td>Uma cadeia de estilos herdados (do pai do nó imediato até a raiz da árvore DOM).</td>
        </tr>
        <tr>
            <td>cssKeyframesRules <br /> <i>opcional</i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td>Uma lista de animações em quadros-chave CSS que correspondem a esse nó.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getPlatformFontsForNode
Solicita informações sobre as fontes da plataforma que usamos para renderizar os textnodes filho no nó fornecido.

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
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
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
            <td>Font</td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td>Estatísticas de uso para todas as fontes empregadas da plataforma.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getComputedStyleForNode
Retorna o estilo calculado de um nó DOM identificado por `nodeId` .

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
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
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
            <td>computedStyle</td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td>Estilo calculado para o nó DOM especificado.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### styleSheetAdded
Disparado sempre que uma folha de estilo de documento ativa é adicionada.

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
            <td>header</td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td>Metainformações da folha de estilos adicionadas.</td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetchanged
Acionado sempre que uma folha de estilos é alterada como resultado da operação do cliente.

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
            <td>styleSheetid</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetRemoved
Disparado sempre que uma folha de estilos de documento ativa é removida.

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
            <td>styleSheetid</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador da folha de estilos removida.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Tipos

### <a name="stylesheetid"></a> StyleSheetid `string`



</p>

---

### <a name="pseudoelementmatches"></a> PseudoElementMatches `object`

Coleção de regras CSS para um único pseudocódigo.

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
            <td>pseudotype</td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td>Pseudo-tipo de elemento.</td>
        </tr>
        <tr>
            <td>corresponde</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Correspondências de regras CSS aplicáveis ao pseudo estilo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> InheritedStyleEntry `object`

Coleção de regras CSS herdada do nó ancestral.

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
            <td>inlinestyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>O estilo embutido do nó ancestral, se houver, na cadeia de herança de estilo.</td>
        </tr>
        <tr>
            <td>matchedCSSRules</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Correspondências de regras CSS correspondentes ao nó ancestral na cadeia de herança de estilo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> RuleMatch `object`

Corresponder dados de uma regra CSS.

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
            <td>das</td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td>Regra CSS na coincidência.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> Value `object`

Dados para um seletor simples (eles são delimitados por vírgulas em uma lista seletora).

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
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Valor do texto.</td>
        </tr>
        <tr>
            <td>gama <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Intervalo de valores no recurso subjacente (se disponível).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> Seletor de seletor `object`

Dados da lista seletor.

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
            <td>seletores</td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td>Seletores na lista.</td>
        </tr>
        <tr>
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Texto do seletor de regra.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> CSSRule `object`

Representação de regra CSS.

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
            <td>styleSheetid <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</td>
        </tr>
        <tr>
            <td>seletor de seletor <br /> <i>opcional</i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td>Dados do seletor de regras.</td>
        </tr>
        <tr>
            <td>Origin <br /> <i>opcional</i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Origem da folha de estilos pai.</td>
        </tr>
        <tr>
            <td>estilo</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Declaração de estilo associada.</td>
        </tr>
        <tr>
            <td>mídia <br /> <i>opcional</i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td>Matriz de lista de mídia (para regras que envolvem consultas de mídia). A matriz enumera consultas de mídia começando com a mais interna, indo para cima.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> SourceRange `object`

Intervalo de texto em um recurso. Todos os números são baseados em zero.

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
            <td>início</td>
            <td><code class="flyout">integer</code></td>
            <td>Linha de início do intervalo.</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Coluna inicial do intervalo (inclusivo).</td>
        </tr>
        <tr>
            <td>Line</td>
            <td><code class="flyout">integer</code></td>
            <td>Linha final do intervalo</td>
        </tr>
        <tr>
            <td>Coluna de EndColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Coluna final do intervalo (exclusivo).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> ShorthandEntry `object`



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
            <td>Nome abreviado.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valor Abreviado.</td>
        </tr>
        <tr>
            <td>principais <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a propriedade tem a anotação "! importante" (implica `false` se estar ausente).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> CSSStyle `object`

Representação de estilo CSS.

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
            <td>styleSheetid <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</td>
        </tr>
        <tr>
            <td>cssProperties</td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td>Propriedades CSS no estilo.</td>
        </tr>
        <tr>
            <td>shorthandEntries</td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td>Valores calculados para todas as abreviações encontradas no estilo.</td>
        </tr>
        <tr>
            <td>cssText <br /> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Texto da declaração de estilo (se disponível).</td>
        </tr>
        <tr>
            <td>gama <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Intervalo de declaração de estilo na folha de estilos delimitadora (se disponível).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> CSSProperty `object`

Dados de declaração de propriedade CSS.

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
            <td>O nome da propriedade.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>O valor da propriedade.</td>
        </tr>
        <tr>
            <td>principais <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a propriedade tem a anotação "! importante" (implica `false` se estar ausente).</td>
        </tr>
        <tr>
            <td>implícito <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a propriedade é implícita (implica `false` se estiver ausente).</td>
        </tr>
        <tr>
            <td>texto <br /> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>O texto completo da propriedade, conforme especificado no estilo.</td>
        </tr>
        <tr>
            <td>parsedOk <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a propriedade é compreendida pelo navegador (implica `true` se estiver ausente).</td>
        </tr>
        <tr>
            <td>ativo <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a propriedade está desabilitada pelo usuário (apenas para Propriedades baseadas na origem).</td>
        </tr>
        <tr>
            <td>gama <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Todo o intervalo de propriedades na declaração de estilo delimitador (se disponível).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> CSSMedia `object`

Descritor de regras de mídia CSS.

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
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Texto de consulta de mídia.</td>
        </tr>
        <tr>
            <td>bibliográfica</td>
            <td><code class="flyout">string</code> <br /> <i>Valores permitidos: mediaRule, importRule, linkedSheet, inlineSheet</i></td>
            <td>Fonte da consulta de mídia: "mediaRule" se especificado por uma regra de @media, "importRule" se especificado por uma regra de @import, "linkedSheet" se especificado por um atributo "Media" na marca de LINK de uma folha de estilos vinculada, "inlineSheet", se especificado por um atributo "Media" em uma marca de estilo da folha de estilos embutida.</td>
        </tr>
        <tr>
            <td>sourceURL <br /> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL do documento que contém a descrição da consulta de mídia.</td>
        </tr>
        <tr>
            <td>gama <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>O intervalo de cabeçalhos de regra (@media ou @import) associado na folha de estilos delimitadora (se disponível).</td>
        </tr>
        <tr>
            <td>styleSheetid <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador da folha de estilos que contém esse objeto (se houver).</td>
        </tr>
        <tr>
            <td>medialist <br /> <i>opcional</i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td>Matriz de consultas de mídia.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> MediaQuery `object`

Descritor de consulta de mídia.

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
            <td>expressão</td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td>Matriz de expressões de consulta de mídia.</td>
        </tr>
        <tr>
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Se a condição de consulta de mídia é satisfeita.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> MediaQueryExpression `object`

Descritor de expressão de consulta de mídia.

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
            <td>value</td>
            <td><code class="flyout">number</code></td>
            <td>Valor da expressão de consulta de mídia.</td>
        </tr>
        <tr>
            <td>organizacional</td>
            <td><code class="flyout">string</code></td>
            <td>Unidades de expressão de consulta de mídia.</td>
        </tr>
        <tr>
            <td>recurso</td>
            <td><code class="flyout">string</code></td>
            <td>Recurso de expressão de consulta de mídia.</td>
        </tr>
        <tr>
            <td>valueRange <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>O intervalo associado do valor do texto na folha de estilos de delimitador (se disponível).</td>
        </tr>
        <tr>
            <td>computedLength <br /> <i>opcional</i></td>
            <td><code class="flyout">number</code></td>
            <td>Duração calculada da expressão de consulta de mídia (se aplicável).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> PlatformFontUsage `object`

Informações sobre a quantidade de glifos que foram renderizados com determinada fonte.

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
            <td>FamilyName</td>
            <td><code class="flyout">string</code></td>
            <td>Nome da família da fonte informado pela plataforma.</td>
        </tr>
        <tr>
            <td>isCustomFont</td>
            <td><code class="flyout">boolean</code></td>
            <td>Indica se a fonte foi baixada ou resolvida localmente.</td>
        </tr>
        <tr>
            <td>glyphCount</td>
            <td><code class="flyout">number</code></td>
            <td>Valor dos glifos renderizados com essa fonte.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> CSSKeyframesRule `object`

Representação de regras de quadros-chave CSS.

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
            <td>animationname</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Nome da animação.</td>
        </tr>
        <tr>
            <td>quadros-chave</td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td>Lista de quadros-chave.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> CSSKeyframeRule `object`

Representação de regra do quadro-chave CSS.

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
            <td>styleSheetid <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</td>
        </tr>
        <tr>
            <td>Origin</td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Origem da folha de estilos pai.</td>
        </tr>
        <tr>
            <td>keytext</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Texto de chave associado.</td>
        </tr>
        <tr>
            <td>estilo</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Declaração de estilo associada.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> CSSComputedStyleProperty `object`



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
            <td>Nome da propriedade de estilo calculado.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valor da propriedade de estilo calculado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> CSSStyleSheetHeader `object`

Metainformação da folha de estilo CSS.

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
            <td>styleSheetid</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>O identificador de folha de estilos.</td>
        </tr>
        <tr>
            <td>sourceURL</td>
            <td><code class="flyout">string</code></td>
            <td>URL do recurso de folha de estilo.</td>
        </tr>
        <tr>
            <td>ativo</td>
            <td><code class="flyout">boolean</code></td>
            <td>Indica se a folha de estilo está desabilitada.</td>
        </tr>
        <tr>
            <td>IsInline</td>
            <td><code class="flyout">boolean</code></td>
            <td>Se essa folha de estilos é criada para marcação de estilo por analisador. Este sinalizador não está definido para marcas de estilo Document. Write.</td>
        </tr>
        <tr>
            <td>início</td>
            <td><code class="flyout">number</code></td>
            <td>Deslocamento de linha da folha de estilos dentro do recurso (com base em zero).</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">number</code></td>
            <td>Deslocamento de coluna da folha de estilos dentro do recurso (com base em zero).</td>
        </tr>
        <tr>
            <td>das</td>
            <td><code class="flyout">number</code></td>
            <td>Tamanho do conteúdo (em caracteres).</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dependências

[DOM](dom.md)
