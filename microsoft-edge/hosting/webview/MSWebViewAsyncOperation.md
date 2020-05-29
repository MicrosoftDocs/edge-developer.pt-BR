---
description: Expõe se a operação foi concluída com sucesso ou falhou
title: Objeto MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: ebb89c0fc645ebcd97357af10af2be650d8218b9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560969"
---
# Objeto MSWebViewAsyncOperation

Expõe se a operação foi concluída com sucesso ou falhou. 

## Eventos

### concluído

Indica que a operação foi concluída. 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### Informações do evento

|            |      |
|------------|------|
|**Interface** | **Evento**
|**Síncrono** |Sim |    
|**Bolhas**     |Não |   
|**Cela**  |Não |        


### erro

Indica que houve um erro com a operação.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### Informações do evento

|            |      |
|------------|------|
|**Interface** | **Evento**
|**Síncrono** |Sim |    
|**Bolhas**     |Não |   
|**Cela**  |Não |            


## Métodos

### start

Chamado para iniciar a tarefa assíncrona. 

```js
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

```js
var error = MSWebViewAsyncOperation.error;
```

#### Valor da propriedade
Tipo: **DOMError**

### OnComplete

O manipulador de eventos **completo** . 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### Valor da propriedade
Tipo: **EventHandler**

### AoOcorrerErro

O manipulador de eventos de **erro** . 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### Valor da propriedade
Tipo: **EventHandler**

### Ready

Descreve o estado pronto do objeto.

Essa propriedade é somente leitura.

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### Valor da propriedade
Tipo: **não assinado curto**

### levar

O resultado da operação.

Essa propriedade é somente leitura.

```js
var result = MSWebViewAsyncOperation.result;
```

#### Valor da propriedade
Tipo: qualquer

### target

O destino da operação. 

Essa propriedade é somente leitura.

```js
var target = MSWebViewAsyncOperation.target;
```

#### Valor da propriedade
Tipo: [ **MSHTMLWebViewElement**](../webview.md)

### tipo

O tipo da operação.

Essa propriedade é somente leitura.

```js
var type = MSWebViewAsyncOperation.type;
```

#### Valor da propriedade
Tipo: **não assinado curto**
