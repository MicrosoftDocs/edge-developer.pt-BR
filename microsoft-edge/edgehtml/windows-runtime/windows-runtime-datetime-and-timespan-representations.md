---
description: Representações de DateTime e TimeSpan do Windows Runtime
title: Representações de DateTime e TimeSpan do Windows Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1ee3d601e727601aba03f2ff7efa532171b8f815
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231536"
---
# <span data-ttu-id="d8ede-103">Representações Windows Runtime DateTime e TimeSpan</span><span class="sxs-lookup"><span data-stu-id="d8ede-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="d8ede-104">A representação JavaScript de datas e horas é diferente da versão do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="d8ede-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="d8ede-105">A estrutura [DateTime][UwpWindowsFoundationDatetime] do Windows Runtime é representada em JavaScript como uma [Data][MDNDate] que tem um repositório de backup que corresponde aos `DateTime` dados \ (e tem um intervalo diferente e uma precisão do JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="d8ede-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="d8ede-106">Se você modificar esse `Date` objeto personalizado, ele se tornará um JavaScript padrão `Date` e perderá a precisão.</span><span class="sxs-lookup"><span data-stu-id="d8ede-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="d8ede-107">`Date`Valores JavaScript podem ser passados para um tempo de execução do Windows `DateTime` e serão verificados por intervalo, o que pode resultar em marshaling de exceções.</span><span class="sxs-lookup"><span data-stu-id="d8ede-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="d8ede-108">A estrutura de [TimeSpan][UwpWindowsFoundationTimespan] do tempo de execução do Windows é convertida em milissegundos e retornada como um número JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d8ede-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="d8ede-109">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8ede-109">See also</span></span>  

[<span data-ttu-id="d8ede-110">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="d8ede-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar o tempo de execução do Windows em JavaScript | Documentos da Microsoft"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Estrutura de DateTime | Documentos da Microsoft"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Estrutura TimeSpan | Documentos da Microsoft"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Data | MDN"  
