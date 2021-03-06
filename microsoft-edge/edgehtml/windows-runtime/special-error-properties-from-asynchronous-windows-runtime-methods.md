---
description: Propriedades de Erro Especiais de Métodos Assíncronos do Windows Runtime
title: Propriedades de Erro Especiais de Métodos Assíncronos do Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9f2fdb007f00c2ab1d1a2050378af80f0075db6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398837"
---
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a>Propriedades especiais de erro de métodos assíncronos do Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Pode ser difícil depurar métodos assíncronos do Windows Runtime em JavaScript, pois o erro pode ser lançado de algum lugar profundo na pilha de chamada.  O objeto JavaScript tem propriedades extras que aparecem somente quando o erro é lançado de um método assíncrono do Windows Runtime quando o aplicativo está em execução no modo `Error` de depuração.  
  
## <a name="special-error-properties"></a>Propriedades de erro especiais  

Um objeto de erro que resulta de uma operação assíncrona do Windows Runtime com falha no modo de depuração tem as seguintes propriedades especiais:  

*   `asyncOpSource` \(Object\) Obtém informações sobre o local original onde a chamada que produziu um erro foi feita.  A propriedade \(String\) exibe o local no código do usuário que originou a operação `asyncOpSource.originatingCall` assíncrona.  
*   asyncOpType \(String\) Obtém o nome do tipo de operação assíncrona que gerou o erro.  
    
Para obter mais informações sobre erros com operações assíncronas, consulte:  

*   [Como lidar com erros com promessas][PreviousVersionsWindowsAppsHh700337]  
*   [Solução de problemas de erros do Windows Runtime][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Como lidar com erros com promessas (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solução de problemas de erros do Windows Runtime (HTML) | Microsoft Docs"  
