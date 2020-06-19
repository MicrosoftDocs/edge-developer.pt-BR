---
description: Contém informações de referenciais sobre a navegação
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752113"
---
# Objeto NavigationEventWithReferrer  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Um objeto que representa um evento acionado quando a navegação é iniciada e a navegação contém um referenciador.  

## Propriedades  

### referência

O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.  

Essa propriedade é somente leitura.  

#### Valor da propriedade  

Tipo: **DOMString**  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### uri  

O URI (Uniform Resource Identifier) do destino da navegação.  

Essa propriedade é somente leitura.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Valor da propriedade  

Tipo: **DOMString**  
