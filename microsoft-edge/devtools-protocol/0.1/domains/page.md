---
description: Referência para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Página Domain-DevTools protocolo versão 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a1cd094baef4571240881a86ecccfdb319fef61b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561357"
---
# Página
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
