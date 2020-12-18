---
description: Propriedades de erro especiais dos métodos do tempo de execução do Windows assíncrono.
title: Propriedades de Erro Especiais de Métodos Assíncronos do Windows Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3557d0097d632f4058e46acbff748f7177d24ab1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231541"
---
# <span data-ttu-id="21a1a-103">Propriedades especiais de erro de métodos assíncronos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="21a1a-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="21a1a-104">Pode ser difícil depurar métodos assíncronos do tempo de execução do Windows em JavaScript, porque o erro pode ser acionado de algum lugar profundo na pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="21a1a-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="21a1a-105">O `Error` objeto JavaScript tem propriedades extras que aparecem somente quando o erro é gerado de um método assíncrono do Windows Runtime quando o aplicativo está em execução no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="21a1a-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="21a1a-106">Propriedades de erro especiais</span><span class="sxs-lookup"><span data-stu-id="21a1a-106">Special error properties</span></span>  

<span data-ttu-id="21a1a-107">Um objeto de erro que resulta de uma operação assíncrona de tempo de execução do Windows com falha no modo de depuração tem as seguintes propriedades especiais:</span><span class="sxs-lookup"><span data-stu-id="21a1a-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="21a1a-108">\ (Objeto \) obtém informações sobre o local original em que a chamada que produziu um erro foi feita.</span><span class="sxs-lookup"><span data-stu-id="21a1a-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="21a1a-109">A propriedade `asyncOpSource.originatingCall` \ (cadeia de caracteres \) exibe o local no código do usuário que originou a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="21a1a-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="21a1a-110">asyncOpType \ (cadeia de caracteres \) Obtém o nome do tipo de operação assíncrona que disparou o erro.</span><span class="sxs-lookup"><span data-stu-id="21a1a-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="21a1a-111">Para obter mais informações sobre erros com operações assíncronas, consulte:</span><span class="sxs-lookup"><span data-stu-id="21a1a-111">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="21a1a-112">Como lidar com erros com promessas</span><span class="sxs-lookup"><span data-stu-id="21a1a-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="21a1a-113">Solução de problemas de erros do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="21a1a-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Como lidar com erros com promessas (HTML) | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solução de problemas de erros do Windows Runtime (HTML) | Documentos da Microsoft"  
