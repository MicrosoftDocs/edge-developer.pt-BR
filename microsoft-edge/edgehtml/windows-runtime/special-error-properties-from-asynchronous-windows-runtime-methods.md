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
# Propriedades especiais de erro de métodos assíncronos do Windows Runtime  

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
