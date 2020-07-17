---
description: Referência para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: d0fbe9cde742d255797a2460b940732ffa5b8f27
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882874"
---
# Schema Domain-DevTools Protocol versão 0,2 (EdgeHTML)  

Fornece informações sobre o esquema de protocolo.

| | |
|-|-|
| [**Métodos**](#methods) | [getdomains](#getdomains) |
| [**Tipos**](#types) | [Domínio](#domain) |
## Métodos

### getdomains
Retorna domínios com suporte.

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
            <td>domínio</td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td>Lista de domínios com suporte.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Tipos

### <a name="domain"></a> Domínio `object`

Descrição do domínio do protocolo.

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
            <td>Nome do domínio.</td>
        </tr>
        <tr>
            <td>version</td>
            <td><code class="flyout">string</code></td>
            <td>Versão do domínio.</td>
        </tr>
    </tbody>
</table>
</p>

---
