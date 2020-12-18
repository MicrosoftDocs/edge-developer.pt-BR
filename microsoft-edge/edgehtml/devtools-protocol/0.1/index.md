---
description: Notas de versão para o protocolo Microsoft Edge DevTools versão 0,1
title: Notas de versão do protocolo DevTools versão 0,1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60e92cb3afa9b10b15c8ebdd520c0061fbb3b366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231691"
---
# Notas de versão do protocolo DevTools versão 0,1

> [!NOTE]
> O protocolo Microsoft Edge DevTools funciona apenas na [atualização de abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

A versão 0,1 do **protocolo Microsoft Edge devtools** fornece uma visualização antecipada para testar a instrumentação do EdgeHTML e a depuração remota básica no novo aplicativo autônomo do [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Assim, requer que você execute a atualização do [Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) ou uma versão mais recente do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

As metas por trás do protocolo DevTools são de três dobras:

 - Fornecer uma API pública para o nosso aplicativo DevTools para anexar ao Microsoft Edge
 - Expandir o acesso da funcionalidade do DevTools a clientes de ferramentas externos
 - Habilitar a depuração remota em todo o intervalo de dispositivos Windows 10 que executam o Microsoft Edge 

Esta versão preliminar fornece a funcionalidade de depuração básica, como a configuração de pontos de interrupção, a depuração por meio do código e a exploração de rastreamentos de pilha. Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis no painel do [**depurador**](../../devtools-guide/debugger.md) , subtração inspeção de cache (para armazenamento da Web, trabalho de serviço, API de cache e IndexedDB). 

Outras funcionalidades do depurador serão adicionadas em versões futuras, seguidas da instrumentação religando outros painéis do [devtools](../index.md) .
