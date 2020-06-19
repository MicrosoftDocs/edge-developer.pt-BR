---
description: Contém informações sobre a navegação do WebView
title: Objeto NavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 785e9646ff400e7ad229046c7030b51420b1d9ad
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752168"
---
# Objeto NavigationEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Um objeto que representa um evento disparado quando a navegação é iniciada.  

## Propriedades  

### uri  

O URI (Uniform Resource Identifier) do destino.  

Essa propriedade é somente leitura.  

```javascript
var uri = NavigationEvent.uri;
```  

#### Valor da propriedade  

Tipo: **DOMString**  
