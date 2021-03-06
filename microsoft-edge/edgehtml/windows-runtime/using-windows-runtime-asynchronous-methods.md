---
description: Usando Métodos Assíncronos do Windows Runtime
title: Usando Métodos Assíncronos do Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c7e8ac4690525ee89a06eccf843531c2c7a20324
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398151"
---
# <a name="using-windows-runtime-asynchronous-methods"></a>Usando métodos assíncronos do Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Muitos métodos do Windows Runtime, especialmente métodos que podem levar muito tempo para ser concluídos, são assíncronos.  Esses métodos geralmente retornam uma ação ou operação assíncrona \(por exemplo, `Windows.Foundation.IAsyncAction` , `Windows.Foundation.IAsyncOperation` , ou `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).  Esses métodos são representados em JavaScript pelo [padrão CommonJS/Promises/A.][CommonjsWikiPromises]  Ou seja, eles retornam um objeto Promise que tem uma função then [,][PreviousVersionsWindowsAppsBr229728]para a qual você deve fornecer uma função que manipulará o resultado se a operação `completed` for bem-sucedida.  Se você não quiser fornecer um manipulador de erros, use a [função done em][PreviousVersionsWindowsAppsHr701079] vez da `then` função.  

> [!IMPORTANT]
> Os recursos do Windows Runtime não estão disponíveis para aplicativos executados no Internet Explorer.  

## <a name="examples-of-asynchronous-methods"></a>Exemplos de métodos assíncronos  

No exemplo a seguir, `then` a função tem um parâmetro que representa o valor concluído do `createResourceAsync` método.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

Nesse caso, se o método falhar, ele retornará uma promessa no estado de `createResourceAsync` erro, mas não lançará uma exceção.  Você pode manipular um erro usando a `then` função da seguinte forma.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

Se você não quiser lidar com o erro explicitamente, mas quiser que ele lance uma exceção, você pode usar a `done` função em vez disso.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Você também pode exibir o progresso feito para a conclusão usando uma terceira função.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
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

Para obter mais informações sobre programação assíncrona, consulte [Programação Assíncrona em JavaScript][PreviousVersionsWindowsAppsHh700330].  

## <a name="see-also"></a>Veja também  

[Usando o Tempo de Execução do Windows no JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usando o Tempo de Execução do Windows no JavaScript | Microsoft Docs"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Método Promise.then | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programação assíncrona em JavaScript (HTML) | Microsoft Docs"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise.done | Microsoft Docs"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promessas | CommonJS Spec Wiki"  
