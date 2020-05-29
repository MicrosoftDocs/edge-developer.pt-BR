---
description: Um evento que é acionado quando uma solicitação HTTP é feita.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560488"
---
# Objeto WebResourceRequestedEvent

Um evento que é acionado quando uma solicitação HTTP é feita.

## Propriedades

### args

Informações sobre a solicitação do recurso. Isso é um [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).

Essa propriedade é somente leitura.

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### Valor da propriedade
Tipo: **qualquer**

