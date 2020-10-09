---
description: Notas de versão para o protocolo Microsoft Edge DevTools versão 0,2
title: Notas de versão do protocolo Microsoft Edge DevTools versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: c4959d2905f95c2bcf98cb78ad67bb88ecfec959
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104739"
---
# Notas de versão do protocolo DevTools versão 0,2

> [!NOTE]
> A versão 0,2 do protocolo Microsoft Edge DevTools funciona apenas na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/getting-started/) .

A versão 0,2 do **protocolo Microsoft Edge devtools** fornece uma visualização para testar a instrumentação do EdgeHTML e a depuração remota básica no novo aplicativo autônomo do [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Assim, requer que você execute a [atualização do Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) ou uma versão mais recente do [Windows Insider Preview](https://insider.windows.com/getting-started/) .

As metas por trás do protocolo DevTools são de três dobras:

 - Fornecer uma API pública para o nosso aplicativo DevTools para anexar ao Microsoft Edge
 - Expandir o acesso da funcionalidade do DevTools a clientes de ferramentas externos
 - Habilitar a depuração remota em todo o intervalo de dispositivos Windows 10 que executam o Microsoft Edge 

A versão 0,2 do protocolo DevTools inclui novos domínios para a depuração de estilo e o layout (somente leitura) e APIs de console, além da funcionalidade de depuração de script principal introduzida na versão 0,1. Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis nos painéis de [**elementos**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) e [**depurador**](../../devtools-guide/debugger.md)  .
