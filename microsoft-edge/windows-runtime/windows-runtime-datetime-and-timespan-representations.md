---
title: Representações de DateTime e TimeSpan do Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d3e138493b80face1238118a99c03f6015a6a8ef
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562507"
---
# <span data-ttu-id="12b4f-102">Representações de DateTime e TimeSpan do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="12b4f-102">Windows Runtime DateTime and TimeSpan Representations</span></span>  

<span data-ttu-id="12b4f-103">A representação JavaScript de datas e horas é diferente da versão do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="12b4f-103">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="12b4f-104">A estrutura [DateTime][UwpWindowsFoundationDatetime] do Windows Runtime é representada em JavaScript como uma [Data][MDNDate] que tem um repositório de backup que corresponde aos `DateTime` dados \ (e tem um intervalo diferente e uma precisão do JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="12b4f-104">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="12b4f-105">Se você modificar esse `Date` objeto personalizado, ele se tornará um JavaScript padrão `Date` e perderá a precisão.</span><span class="sxs-lookup"><span data-stu-id="12b4f-105">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="12b4f-106">`Date`Valores JavaScript podem ser passados para um tempo de execução do Windows `DateTime` e serão verificados por intervalo, o que pode resultar em marshaling de exceções.</span><span class="sxs-lookup"><span data-stu-id="12b4f-106">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="12b4f-107">A estrutura de [TimeSpan][UwpWindowsFoundationTimespan] do tempo de execução do Windows é convertida em milissegundos e retornada como um número JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12b4f-107">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="12b4f-108">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12b4f-108">See Also</span></span>  

[<span data-ttu-id="12b4f-109">Usar o tempo de execução do Windows em JavaScript</span><span class="sxs-lookup"><span data-stu-id="12b4f-109">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar o tempo de execução do Windows em JavaScript"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Estrutura de DateTime"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Estrutura TimeSpan"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Data | MDN"  
