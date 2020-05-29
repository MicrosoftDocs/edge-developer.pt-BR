---
title: Usando métodos assíncronos do tempo de execução do Windows
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6d0f174d22d0d13571d78bc215356ad90a0ae7fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562508"
---
# Usando métodos assíncronos do tempo de execução do Windows  

Muitos métodos do tempo de execução do Windows, especialmente métodos que podem levar muito tempo para serem concluídos, são assíncronos.  Esses métodos geralmente retornam uma ação ou operação assíncrona (por exemplo,,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` ou `Windows.Foundation.IAsyncOperationWithProgress` ).  Esses métodos são representados em JavaScript pelo [padrão CommonJS/promete/A][CommonjsWikiPromises].  Ou seja, eles retornam um objeto Promise que tem uma [função function][PreviousVersionsWindowsAppsBr229728], para a qual você deve fornecer uma `completed` função que manipula o resultado se a operação for bem-sucedida.  Se você não quiser fornecer um identificador de erro, use a [função Done][PreviousVersionsWindowsAppsHr701079] em vez da `then` função.  

> [!IMPORTANT]
> Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.  

## Exemplos de métodos assíncronos  

No exemplo a seguir, a `then` função usa um parâmetro que representa o valor concluído do `createResourceAsync` método.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

Nesse caso, se o `createResourceAsync` método falhar, ele retornará uma promessa no estado do erro, mas não lança uma exceção.  Você pode manipular um erro usando a `then` função da seguinte maneira.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

Se não quiser manipular o erro explicitamente, mas quiser que ele Acione uma exceção, você pode usar a `done` função em vez disso.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Você também pode exibir o progresso feito em direção à conclusão usando uma terceira função.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
            },
    // Error.
            function(error) {
               alert("Failed to create a resource.");
            },
    // Progress.
            function(progress, resultSoFar) {
               setProgressBar(progress);
            });
```  

Para obter mais informações sobre programação assíncrona, consulte [programação assíncrona em JavaScript][PreviousVersionsWindowsAppsHh700330].  

## Consulte também  

[Usar o tempo de execução do Windows em JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar o tempo de execução do Windows em JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promessa e método"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programação assíncrona em JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise. Done"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promessas | Wiki de especificações CommonJS"  
