---
description: Referência para o domínio de sobreposição. Domínio sobreposto expõe a interação visual adorners e seleção de nós
title: Sobreposição de protocolo de domínio-DevTools versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: a7657e2abc99e45894f19f6557f12f78f8ee9c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561331"
---
# Sobreposição
Domínio sobreposto expõe a interação visual adorners e seleção de nós

| | |
|-|-|
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar](#disable)e [setinspecionámode](#setinspectmode) |
| [**Eventos**](#events) | [inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested) |
| [**Dependências**](#dependencies) | [DOM](dom.md) |
## Métodos

### Habilitar
Permite a emissão de relatórios <code>nodeHighlightRequested</code> e <code>inspectElementRequested</code> eventos

</p>

---

### Desabilitar 
Desabilita o relatório de eventos de domínio sobrepostos

</p>

---

### setinspecionámode
Define o modo de seleção de elementos do cliente

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
            <td>modo</td>
            <td><code class="flyout">string</code></td>
            <td>O modo de inspeção.  Os valores válidos são ' searchForNode ' e ' nenhum '.</td>
        </tr>
        <tr>
            <td>highlightConfig <br/> <i>opcional</i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td>A configuração de destaque a ser usada ao inspecionar</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### inspectNodeRequested
Notifica o cliente que o usuário pediu para inspecionar um nó específico

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
            <td>backendNodeId</td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td>A ID do nó back-end do nó solicitado</td>
        </tr>
    </tbody>
</table>
</p>

---

### nodeHighlightRequested
Indica que o usuário passou o mouse sobre o nó e pode inspecionar o nó

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
            <td>A ID do nó que está sendo considerado</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dependências

[DOM](dom.md)