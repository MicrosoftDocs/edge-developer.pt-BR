---
description: Expõe se a operação foi concluída com sucesso ou falhou
title: Objeto MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: d6e03af2a0205938f19120076aa0ad622539d7e5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752119"
---
# Objeto MSWebViewAsyncOperation  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Expõe se a operação foi concluída com sucesso ou falhou.  

## Eventos  

### concluído  

Indica que a operação foi concluída.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | **Evento** |  
| **Síncrono** |Sim |  
| **Bolhas** |Não |   
| **Cela** |Não |  

### erro  

Indica que houve um erro com a operação.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | **Evento** |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |  
| **Cela** | Não |  

## Métodos  

### start  

Chamado para iniciar a tarefa assíncrona.  

```javascript
MSWebViewAsyncOperation.start();
```  

### Parâmetros  

Esse método não tem parâmetros.  

### Valor de retorno  

Esse método não retorna um valor.  

## Propriedades  

### erro  

O erro que ocorreu.  

Essa propriedade é somente leitura.  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### Valor da propriedade  

Tipo: **DOMError**  

### OnComplete  

O manipulador de eventos **completo** .  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### Valor da propriedade  

Tipo: **EventHandler**  

### AoOcorrerErro  

O manipulador de eventos de **erro** .  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### Valor da propriedade  

Tipo: **EventHandler**  

### Ready  

Descreve o estado pronto do objeto.  

Essa propriedade é somente leitura.  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### Valor da propriedade  

Tipo: **não assinado curto**  

### levar  

O resultado da operação.  

Essa propriedade é somente leitura.  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### Valor da propriedade  

Tipo: qualquer  

### target  

O destino da operação.  

Essa propriedade é somente leitura.  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### Valor da propriedade  

Tipo: [ **MSHTMLWebViewElement**](../webview.md)  

### tipo  

O tipo da operação.  

Essa propriedade é somente leitura.  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### Valor da propriedade  

Tipo: **não assinado curto**  
