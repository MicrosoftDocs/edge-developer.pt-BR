---
description: Referência para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 83d7019d18ccce1c81b67aafdcafe1a8566694ea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561351"
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

---
