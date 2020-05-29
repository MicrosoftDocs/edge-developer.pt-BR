---
description: Contém informações sobre a navegação da WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560965"
---
# Objeto NavigationCompletedEvent

Um objeto que representa um evento disparado quando o [WebView](../webview.md) concluiu o carregamento do conteúdo atual ou se houve falha na navegação.

## Propriedades
    
### uri

O URI (Uniform Resource Identifier) da navegação.

Essa propriedade é somente leitura.

```js
var uri = NavigationCompletedEvent.uri;
```

#### Valor da propriedade
Tipo: **DOMString**

### IsSuccess

Obtém um valor que indica se a navegação foi concluída com sucesso.

Essa propriedade é somente leitura

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### Valor da propriedade
Tipo: **booliano**

### webErrorStatus

Se a navegação não tiver sido bem-sucedida, obtém um valor que indica o motivo.

Essa propriedade é somente leitura

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### Valor da propriedade
Tipo: **unsigned long**
