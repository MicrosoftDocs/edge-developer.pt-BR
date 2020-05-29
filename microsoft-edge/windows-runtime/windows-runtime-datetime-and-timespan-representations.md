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
# Representações de DateTime e TimeSpan do Windows Runtime  

A representação JavaScript de datas e horas é diferente da versão do Windows Runtime.  A estrutura [DateTime][UwpWindowsFoundationDatetime] do Windows Runtime é representada em JavaScript como uma [Data][MDNDate] que tem um repositório de backup que corresponde aos `DateTime` dados \ (e tem um intervalo diferente e uma precisão do JavaScript `Date` \).  Se você modificar esse `Date` objeto personalizado, ele se tornará um JavaScript padrão `Date` e perderá a precisão.  `Date`Valores JavaScript podem ser passados para um tempo de execução do Windows `DateTime` e serão verificados por intervalo, o que pode resultar em marshaling de exceções.  

 A estrutura de [TimeSpan][UwpWindowsFoundationTimespan] do tempo de execução do Windows é convertida em milissegundos e retornada como um número JavaScript.  

## Consulte também  

[Usar o tempo de execução do Windows em JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar o tempo de execução do Windows em JavaScript"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Estrutura de DateTime"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Estrutura TimeSpan"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Data | MDN"  
