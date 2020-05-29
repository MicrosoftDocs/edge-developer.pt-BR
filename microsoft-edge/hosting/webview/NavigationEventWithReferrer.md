---
description: Contém informações de referenciais sobre a navegação
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560959"
---
# Objeto NavigationEventWithReferrer

Um objeto que representa um evento acionado quando a navegação é iniciada e a navegação contém um referenciador.

## Propriedades

### referência

O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.

Essa propriedade é somente leitura.

#### Valor da propriedade
Tipo: **DOMString**


```js
var referer = NavigationEventWithReferrer.referer;
```

### uri

O URI (Uniform Resource Identifier) do destino da navegação.

Essa propriedade é somente leitura.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Valor da propriedade
Tipo: **DOMString**
