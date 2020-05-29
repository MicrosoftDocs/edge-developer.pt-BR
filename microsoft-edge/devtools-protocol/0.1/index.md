---
description: Notas de versão para o protocolo Microsoft Edge DevTools versão 0,1
title: Notas de versão do protocolo DevTools versão 0,1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 29dc8f1b0ba67cb2b3155cb2135d488609e9bff9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561348"
---
# Notas de versão do protocolo DevTools versão 0,1

> [!NOTE]
> O protocolo Microsoft Edge DevTools funciona apenas na [atualização de abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

A versão 0,1 do **protocolo Microsoft Edge devtools** fornece uma visualização antecipada para testar a instrumentação do EdgeHTML e a depuração remota básica no novo aplicativo autônomo do [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Assim, requer que você execute a atualização do [Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) ou uma versão mais recente do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

As metas por trás do protocolo DevTools são de três dobras:

 - Fornecer uma API pública para o nosso aplicativo DevTools para anexar ao Microsoft Edge
 - Expandir o acesso da funcionalidade do DevTools a clientes de ferramentas externos
 - Habilitar a depuração remota na faixa de dispositivos Windows 10 que executam o Edge Micrsoft 

Esta versão preliminar fornece a funcionalidade de depuração básica, como a configuração de pontos de interrupção, a depuração por meio do código e a exploração de rastreamentos de pilha. Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis no painel do [**depurador**](../../devtools-guide/debugger.md) , subtração inspeção de cache (para armazenamento da Web, trabalho de serviço, API de cache e IndexedDB). 

Outras funcionalidades do depurador serão adicionadas em versões futuras, seguidas da instrumentação religando outros painéis do [devtools](../../devtools-guide.md) .
