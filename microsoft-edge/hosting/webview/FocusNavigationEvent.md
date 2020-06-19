---
description: O objeto despachado de um evento Focus que contém o motivo e a localização da navegação
title: Objeto FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752161"
---
# Objeto FocusNavigationEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

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

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### Valor da propriedade  

Tipo: **NavigationReason**  

### originHeight  

O local da altura da origem do elemento a receber o foco.  

Essa propriedade é somente leitura.  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### Valor da propriedade  

Tipo: **float**  

### originLeft  

O local de origem do elemento para receber o foco.  

Essa propriedade é somente leitura.  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### Valor da propriedade  

Tipo: **float**  

### originTop  

O local de origem superior do elemento a receber o foco.  

Essa propriedade é somente leitura.  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### Valor da propriedade  

Tipo: **float**  

### originWidth  

O local da largura de origem do elemento a receber o foco.  

Essa propriedade é somente leitura.  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### Valor da propriedade  

Tipo: **float**  
