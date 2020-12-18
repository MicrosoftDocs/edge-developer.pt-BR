---
description: Referência para o domínio DOMDebugger. A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM. A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.
title: DOMDebugger Domain-DevTools Protocol versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231308"
---
# DOMDebugger

A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM. A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.

| | |
|-|-|
| [**Métodos**](#methods) | [setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint) |
## Métodos

### setInstrumentationBreakpoint
<span><b>Experimentais. </b></span>Define um ponto de interrupção em um evento nativo específico.

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
            <td>EventName</td>
            <td><code class="flyout">string</code></td>
            <td>Nome da instrumentação para parar. Valores válidos: "scriptFirstStatement".</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeInstrumentationBreakpoint
<span><b>Experimentais. </b></span>Remove um ponto de interrupção em um evento nativo específico.

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
            <td>EventName</td>
            <td><code class="flyout">string</code></td>
            <td>Nome da instrumentação para parar. Valores válidos: "scriptFirstStatement".</td>
        </tr>
    </tbody>
</table>
</p>

---
