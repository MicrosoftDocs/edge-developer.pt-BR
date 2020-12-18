---
description: Usar métodos assíncronos do tempo de execução do Windows.
title: Usando Métodos Assíncronos do Windows Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 26ed26e07049a9488aebe5fda92a65550474b51c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231537"
---
# <span data-ttu-id="0a0e8-103">Usando métodos assíncronos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="0a0e8-103">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="0a0e8-104">Muitos métodos do tempo de execução do Windows, especialmente métodos que podem levar muito tempo para serem concluídos, são assíncronos.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-104">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="0a0e8-105">Esses métodos geralmente retornam uma ação assíncrona ou operação \ (por exemplo,,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` ou `Windows.Foundation.IAsyncOperationWithProgress` \).</span><span class="sxs-lookup"><span data-stu-id="0a0e8-105">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="0a0e8-106">Esses métodos são representados em JavaScript pelo [padrão CommonJS/promete/A][CommonjsWikiPromises].</span><span class="sxs-lookup"><span data-stu-id="0a0e8-106">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="0a0e8-107">Ou seja, eles retornam um objeto Promise que tem uma [função function][PreviousVersionsWindowsAppsBr229728], para a qual você deve fornecer uma `completed` função que manipula o resultado se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-107">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="0a0e8-108">Se você não quiser fornecer um identificador de erro, use a [função Done][PreviousVersionsWindowsAppsHr701079] em vez da `then` função.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-108">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0a0e8-109">Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-109">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="0a0e8-110">Exemplos de métodos assíncronos</span><span class="sxs-lookup"><span data-stu-id="0a0e8-110">Examples of asynchronous methods</span></span>  

<span data-ttu-id="0a0e8-111">No exemplo a seguir, a `then` função usa um parâmetro que representa o valor concluído do `createResourceAsync` método.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-111">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="0a0e8-112">Nesse caso, se o `createResourceAsync` método falhar, ele retornará uma promessa no estado do erro, mas não lança uma exceção.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-112">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="0a0e8-113">Você pode manipular um erro usando a `then` função da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-113">You can handle an error by using the `then` function as follows.</span></span>  

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

<span data-ttu-id="0a0e8-114">Se não quiser manipular o erro explicitamente, mas quiser que ele Acione uma exceção, você pode usar a `done` função em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-114">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="0a0e8-115">Você também pode exibir o progresso feito em direção à conclusão usando uma terceira função.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-115">You can also display the progress made towards completion by using a third function.</span></span>  

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

<span data-ttu-id="0a0e8-116">Para obter mais informações sobre programação assíncrona, consulte [programação assíncrona em JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="0a0e8-116">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <span data-ttu-id="0a0e8-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0a0e8-117">See also</span></span>  

[<span data-ttu-id="0a0e8-118">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="0a0e8-118">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar o tempo de execução do Windows em JavaScript | Documentos da Microsoft"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promessa. depois, método | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programação assíncrona em JavaScript (HTML) | Documentos da Microsoft"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Método Promise. Done | Documentos da Microsoft"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promessas | Wiki de especificações CommonJS"  
