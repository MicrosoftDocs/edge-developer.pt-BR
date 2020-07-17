---
description: Referência para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Page Domain-DevTools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1602673eae1c04f60046a898dbadeab1b59f9ce5
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882937"
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
