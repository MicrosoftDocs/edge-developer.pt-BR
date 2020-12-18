---
description: DevTools Protocol Version 0,2 (EdgeHTML) Reference para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 53038a02844fafc9550a6ac26303620a1a0183f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231302"
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
