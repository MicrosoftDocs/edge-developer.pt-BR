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
# Propriedades de erro especiais dos métodos do tempo de execução do Windows assíncrono  

Pode ser difícil depurar métodos assíncronos do tempo de execução do Windows em JavaScript, porque o erro pode ser acionado de algum lugar profundo na pilha de chamadas. O `Error` objeto JavaScript tem propriedades extras que aparecem somente quando o erro é gerado de um método assíncrono do Windows Runtime quando o aplicativo está em execução no modo de depuração.  
  
## Propriedades de erro especiais  

Um objeto de erro que resulta de uma operação assíncrona de tempo de execução do Windows com falha no modo de depuração tem as seguintes propriedades especiais:  

*   `asyncOpSource` \ (Objeto \) obtém informações sobre o local original em que a chamada que produziu um erro foi feita. A propriedade `asyncOpSource.originatingCall` \ (cadeia de caracteres \) exibe o local no código do usuário que originou a operação assíncrona.  
*   asyncOpType \ (cadeia de caracteres \) Obtém o nome do tipo de operação assíncrona que disparou o erro.  
    
Para obter mais informações sobre erros com operações assíncronas, consulte:  
  
*   [Como lidar com erros com promessas][PreviousVersionsWindowsAppsHh700337]  
*   [Solução de problemas de erros do Windows Runtime][PreviousVersionsWindowsAppsHh974350]  

<!-- image links -->  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Como lidar com erros com promessas (HTML)"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solução de problemas de erros do Windows Runtime (HTML)"  
