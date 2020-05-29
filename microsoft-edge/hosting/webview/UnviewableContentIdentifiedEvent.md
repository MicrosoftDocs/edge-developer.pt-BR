---
description: Indica que o WebView está tentando baixar um arquivo sem suporte.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560491"
---
# Objeto UnviewableContentIdentifiedEvent

Indica que o [WebView](../webview.md) está tentando navegar para um arquivo de um tipo de conteúdo sem suporte. 

## Propriedades

### mediaType

Obtém o tipo de conteúdo do conteúdo inviewável.

Essa propriedade é somente leitura

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### Valor da propriedade
Tipo: **DOMString**

### referência

O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.

Essa propriedade é somente leitura.


```js
var referer = NavigationEventWithReferrer.referer;
```

#### Valor da propriedade
Tipo: **DOMString**

### uri

O URI (Uniform Resource Identifier) do destino da navegação.

Essa propriedade é somente leitura.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Valor da propriedade
Tipo: **DOMString**
