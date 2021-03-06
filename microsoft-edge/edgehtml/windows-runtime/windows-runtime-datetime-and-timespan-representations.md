---
description: Representações de DateTime e TimeSpan do Windows Runtime
title: Representações de DateTime e TimeSpan do Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
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
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c2627826755f041a440112c3390ecb17d1f703ce
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398123"
---
# <a name="windows-runtime-datetime-and-timespan-representations"></a><span data-ttu-id="5789b-103">Representações Windows Runtime DateTime e TimeSpan</span><span class="sxs-lookup"><span data-stu-id="5789b-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="5789b-104">A representação JavaScript de datas e horas é diferente da versão do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="5789b-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="5789b-105">A estrutura do Windows Runtime [DateTime][UwpWindowsFoundationDatetime] é representada em JavaScript como uma [Data][MDNDate] que tem um armazenamento de suporte que corresponde aos dados \(e tem um intervalo e precisão diferentes do `DateTime` JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="5789b-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="5789b-106">Se você modificar esse objeto `Date` personalizado, ele se tornará um JavaScript padrão `Date` e perderá precisão.</span><span class="sxs-lookup"><span data-stu-id="5789b-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="5789b-107">Os valores JavaScript podem ser passados para um Tempo de Execução do Windows e serão verificados pelo intervalo, o que pode resultar em `Date` `DateTime` exceções de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="5789b-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

<span data-ttu-id="5789b-108">A estrutura do Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] é convertida em milissegundos e retornada como um número JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5789b-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5789b-109">Veja também</span><span class="sxs-lookup"><span data-stu-id="5789b-109">See also</span></span>  

[<span data-ttu-id="5789b-110">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="5789b-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usando o Tempo de Execução do Windows no JavaScript | Microsoft Docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Estrutura do DateTime | Microsoft Docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan Struct | Microsoft Docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Data | MDN"  
