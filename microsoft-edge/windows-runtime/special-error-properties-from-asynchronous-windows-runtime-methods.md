---
title: Propriedades de Erro Especiais de Métodos Assíncronos do Windows Runtime
ms.custom: ''
ms.date: 07/29/2020
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
ms.openlocfilehash: a1fccf1cec811501b94e7da4aa20b69d93754f62
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942071"
---
# Propriedades de erro especiais dos métodos do tempo de execução do Windows assíncrono  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Pode ser difícil depurar métodos assíncronos do tempo de execução do Windows em JavaScript, porque o erro pode ser acionado de algum lugar profundo na pilha de chamadas.  O `Error` objeto JavaScript tem propriedades extras que aparecem somente quando o erro é gerado de um método assíncrono do Windows Runtime quando o aplicativo está em execução no modo de depuração.  
  
## Propriedades de erro especiais  

Um objeto de erro que resulta de uma operação assíncrona de tempo de execução do Windows com falha no modo de depuração tem as seguintes propriedades especiais:  

*   `asyncOpSource` \ (Objeto \) obtém informações sobre o local original em que a chamada que produziu um erro foi feita.  A propriedade `asyncOpSource.originatingCall` \ (cadeia de caracteres \) exibe o local no código do usuário que originou a operação assíncrona.  
*   asyncOpType \ (cadeia de caracteres \) Obtém o nome do tipo de operação assíncrona que disparou o erro.  
    
Para obter mais informações sobre erros com operações assíncronas, consulte:  
  
*   [Como lidar com erros com promessas][PreviousVersionsWindowsAppsHh700337]  
*   [Solução de problemas de erros do Windows Runtime][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Como lidar com erros com promessas (HTML) | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solução de problemas de erros do Windows Runtime (HTML) | Documentos da Microsoft"  
