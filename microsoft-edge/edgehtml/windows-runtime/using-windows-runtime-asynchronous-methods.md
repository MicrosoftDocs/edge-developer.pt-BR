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
# <a name="using-windows-runtime-asynchronous-methods"></a><span data-ttu-id="87aa9-103">Usando métodos assíncronos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="87aa9-103">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="87aa9-104">Muitos métodos do Windows Runtime, especialmente métodos que podem levar muito tempo para ser concluídos, são assíncronos.</span><span class="sxs-lookup"><span data-stu-id="87aa9-104">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="87aa9-105">Esses métodos geralmente retornam uma ação ou operação assíncrona \(por exemplo, `Windows.Foundation.IAsyncAction` , `Windows.Foundation.IAsyncOperation` , ou `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).</span><span class="sxs-lookup"><span data-stu-id="87aa9-105">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="87aa9-106">Esses métodos são representados em JavaScript pelo [padrão CommonJS/Promises/A.][CommonjsWikiPromises]</span><span class="sxs-lookup"><span data-stu-id="87aa9-106">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="87aa9-107">Ou seja, eles retornam um objeto Promise que tem uma função then [,][PreviousVersionsWindowsAppsBr229728]para a qual você deve fornecer uma função que manipulará o resultado se a operação `completed` for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="87aa9-107">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="87aa9-108">Se você não quiser fornecer um manipulador de erros, use a [função done em][PreviousVersionsWindowsAppsHr701079] vez da `then` função.</span><span class="sxs-lookup"><span data-stu-id="87aa9-108">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="87aa9-109">Os recursos do Windows Runtime não estão disponíveis para aplicativos executados no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="87aa9-109">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="examples-of-asynchronous-methods"></a><span data-ttu-id="87aa9-110">Exemplos de métodos assíncronos</span><span class="sxs-lookup"><span data-stu-id="87aa9-110">Examples of asynchronous methods</span></span>  

<span data-ttu-id="87aa9-111">No exemplo a seguir, `then` a função tem um parâmetro que representa o valor concluído do `createResourceAsync` método.</span><span class="sxs-lookup"><span data-stu-id="87aa9-111">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="87aa9-112">Nesse caso, se o método falhar, ele retornará uma promessa no estado de `createResourceAsync` erro, mas não lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="87aa9-112">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="87aa9-113">Você pode manipular um erro usando a `then` função da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="87aa9-113">You can handle an error by using the `then` function as follows.</span></span>  

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

<span data-ttu-id="87aa9-114">Se você não quiser lidar com o erro explicitamente, mas quiser que ele lance uma exceção, você pode usar a `done` função em vez disso.</span><span class="sxs-lookup"><span data-stu-id="87aa9-114">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="87aa9-115">Você também pode exibir o progresso feito para a conclusão usando uma terceira função.</span><span class="sxs-lookup"><span data-stu-id="87aa9-115">You can also display the progress made towards completion by using a third function.</span></span>  

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

<span data-ttu-id="87aa9-116">Para obter mais informações sobre programação assíncrona, consulte [Programação Assíncrona em JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="87aa9-116">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <a name="see-also"></a><span data-ttu-id="87aa9-117">Veja também</span><span class="sxs-lookup"><span data-stu-id="87aa9-117">See also</span></span>  

[<span data-ttu-id="87aa9-118">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="87aa9-118">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usando o Tempo de Execução do Windows no JavaScript | Microsoft Docs"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Método Promise.then | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programação assíncrona em JavaScript (HTML) | Microsoft Docs"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise.done | Microsoft Docs"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promessas | CommonJS Spec Wiki"  
