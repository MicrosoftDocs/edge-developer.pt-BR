---
description: Referência para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: df86e6669956c14b7c905514fc44376f71eaa993
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561326"
---
# Esquema
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
