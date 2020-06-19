---
description: Indica que o WebView está tentando baixar um arquivo sem suporte.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752010"
---
# Objeto UnviewableContentIdentifiedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Indica que o [WebView](../webview.md) está tentando navegar para um arquivo de um tipo de conteúdo sem suporte.  

## Propriedades  

### mediaType  

Obtém o tipo de conteúdo do conteúdo inviewável.  

Essa propriedade é somente leitura  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### Valor da propriedade  

Tipo: **DOMString**  

### referência  

O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.  

Essa propriedade é somente leitura.  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### Valor da propriedade  

Tipo: **DOMString**  

### uri  

O URI (Uniform Resource Identifier) do destino da navegação.  

Essa propriedade é somente leitura.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Valor da propriedade  

Tipo: **DOMString**  
