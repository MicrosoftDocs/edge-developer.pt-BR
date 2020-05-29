---
description: Referência para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Página Domain-DevTools protocolo versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 688cc1fcfce0b81c5eed0c858a4a60b4754c49a4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561333"
---
# Página
Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.

| | |
|-|-|
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar](#disable), [navegar](#navigate), [getFrameTree](#getframetree) |
| [**Eventos**](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |
| [**Tipos**](#types) | [Frameid](#frameid), [frame](#frame), [FrameTree](#frametree) |
## Métodos

### Habilitar
Habilita as notificações de domínio da página.

</p>

---

### Desabilitar 
Desativa as notificações de domínio da página.

</p>

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
        <tr>
            <td>frameid <br/> <i>opcional</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ID do quadro para navegar. Se não for especificado, navegará na página superior.</td>
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
            <td>ID do quadro que será navegada.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getFrameTree
Retorna a estrutura da árvore de quadros atual.

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
            <td>frameTree</td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td>Apresentar estrutura de árvore de quadros.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### frameAttached
Disparado quando o quadro é anexado ao seu pai.

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
            <td>frameid</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ID do quadro que foi anexado.</td>
        </tr>
        <tr>
            <td>parentFrameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador de quadro pai.</td>
        </tr>
        <tr>
            <td>empilh <br/> <i>opcional</i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td>Rastreamento de pilha JavaScript de quando o quadro foi anexado, somente defina se o quadro foi iniciado a partir do script.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameDetached
Disparado quando o quadro é separado de seu pai.

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
            <td>frameid</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ID do quadro que foi desconectado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameNavigated
Disparado após a conclusão da navegação do quadro.

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
            <td>tempo</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Objeto frame.</td>
        </tr>
    </tbody>
</table>
</p>

---

### loadEventFired
Corresponde ao evento Window. OnLoad.

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
            <td>carimbo</td>
            <td><code class="flyout">number</code></td>
            <td>Número de milissegundos desde a época.</td>
        </tr>
    </tbody>
</table>
</p>

---

### domContentEventFired
Corresponde ao evento Document. onDOMContentLoaded.

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
            <td>carimbo</td>
            <td><code class="flyout">number</code></td>
            <td>Número de milissegundos desde a época.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Tipos

### <a name="frameid"></a> Frameid `string`

Identificador de quadro exclusivo.

</p>

---

### <a name="frame"></a> Quadro `object`

Informações sobre o quadro na página.

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
            <td>id</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador exclusivo do quadro.</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>opcional</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificador exclusivo do quadro pai.</td>
        </tr>
        <tr>
            <td>name <br/> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nome do quadro, conforme especificado na marca.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL do documento de quadro.</td>
        </tr>
        <tr>
            <td>securityOrigin</td>
            <td><code class="flyout">string</code></td>
            <td>Origem de segurança do documento de quadro.</td>
        </tr>
        <tr>
            <td>MIME</td>
            <td><code class="flyout">string</code></td>
            <td>MimeType do documento de quadro conforme determinado pelo navegador.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> FrameTree `object`

Informações sobre a hierarquia de quadros.

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
            <td>tempo</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Informações de quadro para este item de árvore.</td>
        </tr>
        <tr>
            <td>childFrames <br/> <i>opcional</i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td>Quadros filho.</td>
        </tr>
    </tbody>
</table>
</p>

---
