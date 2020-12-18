---
description: Referência do protocolo DevTools versão 0,1 (EdgeHTML) para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Page Domain-DevTools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231697"
---
# Page Domain-DevTools Protocol Version 0,1 (EdgeHTML)  

Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.

| | |
|-|-|
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar](#disable), [navegar](#navigate) |
| [**Tipos**](#types) | [Frameid](#frameid) |
## Métodos

### Habilitar
Habilita as notificações de domínio da página.


---

### Desabilitar 
Desativa as notificações de domínio da página.


---

### navegar
Navega a página atual para a URL fornecida.

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
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL para navegar na página.</td>
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
            <td>frameid</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b>Experimentais. </b></span>ID do quadro que será navegada.</td>
        </tr>
    </tbody>
</table>

---

## Tipos

### <a name="frameid"></a> Frameid `string`

Identificador de quadro exclusivo.


---
