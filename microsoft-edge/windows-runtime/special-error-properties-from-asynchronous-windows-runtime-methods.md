---
title: Propriedades de erro especiais dos métodos do tempo de execução do Windows assíncrono
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5cf2604e26c84e769cf44e0879ee137cbfbe8b90
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562513"
---
# <span data-ttu-id="2eecd-102">Propriedades de erro especiais dos métodos do tempo de execução do Windows assíncrono</span><span class="sxs-lookup"><span data-stu-id="2eecd-102">Special Error Properties from Asynchronous Windows Runtime Methods</span></span>  

<span data-ttu-id="2eecd-103">Pode ser difícil depurar métodos assíncronos do tempo de execução do Windows em JavaScript, porque o erro pode ser acionado de algum lugar profundo na pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2eecd-103">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span> <span data-ttu-id="2eecd-104">O `Error` objeto JavaScript tem propriedades extras que aparecem somente quando o erro é gerado de um método assíncrono do Windows Runtime quando o aplicativo está em execução no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="2eecd-104">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="2eecd-105">Propriedades de erro especiais</span><span class="sxs-lookup"><span data-stu-id="2eecd-105">Special Error Properties</span></span>  

<span data-ttu-id="2eecd-106">Um objeto de erro que resulta de uma operação assíncrona de tempo de execução do Windows com falha no modo de depuração tem as seguintes propriedades especiais:</span><span class="sxs-lookup"><span data-stu-id="2eecd-106">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="2eecd-107">\ (Objeto \) obtém informações sobre o local original em que a chamada que produziu um erro foi feita.</span><span class="sxs-lookup"><span data-stu-id="2eecd-107">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span> <span data-ttu-id="2eecd-108">A propriedade `asyncOpSource.originatingCall` \ (cadeia de caracteres \) exibe o local no código do usuário que originou a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2eecd-108">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="2eecd-109">asyncOpType \ (cadeia de caracteres \) Obtém o nome do tipo de operação assíncrona que disparou o erro.</span><span class="sxs-lookup"><span data-stu-id="2eecd-109">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="2eecd-110">Para obter mais informações sobre erros com operações assíncronas, consulte:</span><span class="sxs-lookup"><span data-stu-id="2eecd-110">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="2eecd-111">Como lidar com erros com promessas</span><span class="sxs-lookup"><span data-stu-id="2eecd-111">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="2eecd-112">Solução de problemas de erros do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2eecd-112">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- image links -->  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Como lidar com erros com promessas (HTML)"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solução de problemas de erros do Windows Runtime (HTML)"  
