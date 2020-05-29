---
description: Referência para o domínio DOMDebugger. A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM. A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.
title: DOMDebugger Domain-DevTools Protocol versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561332"
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
