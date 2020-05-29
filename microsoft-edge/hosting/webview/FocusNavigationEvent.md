---
description: O objeto despachado de um evento Focus que contém o motivo e a localização da navegação
title: Objeto FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560976"
---
# Objeto FocusNavigationEvent

O objeto despachado da [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) que contém o [**NavigationReason**](#navigationreason) e o local. 

## Métodos

### requestFocus

Chamado para mover o foco do aplicativo para o WebView.

### Parâmetros

Esse método não tem parâmetros.

### Valor de retorno

Esse método não retorna um valor.

## Propriedades
    
### navigationReason

O tipo enumerado **NavigationReason**, "Left", "up", "Right" ou "Down". 

Essa propriedade é somente leitura.

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### Valor da propriedade
Tipo: **NavigationReason**

### originHeight

O local da altura da origem do elemento a receber o foco.

Essa propriedade é somente leitura.

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### Valor da propriedade
Tipo: **float**

### originLeft

O local de origem do elemento para receber o foco.

Essa propriedade é somente leitura.

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### Valor da propriedade
Tipo: **float**

### originTop

O local de origem superior do elemento a receber o foco.

Essa propriedade é somente leitura.

```js
var originTop = FocusNavigationEvent.originTop;
```

#### Valor da propriedade
Tipo: **float**

### originWidth

O local da largura de origem do elemento a receber o foco.

Essa propriedade é somente leitura.

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### Valor da propriedade
Tipo: **float**

