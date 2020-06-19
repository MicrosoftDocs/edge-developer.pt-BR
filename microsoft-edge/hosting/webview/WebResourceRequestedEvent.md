---
description: Um evento que é acionado quando uma solicitação HTTP é feita.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751979"
---
# Objeto WebResourceRequestedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Um evento que é acionado quando uma solicitação HTTP é feita.  

## Propriedades  

### args  

Informações sobre a solicitação do recurso.  Isso é um [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).  

Essa propriedade é somente leitura.  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### Valor da propriedade  

Tipo: **qualquer**  
