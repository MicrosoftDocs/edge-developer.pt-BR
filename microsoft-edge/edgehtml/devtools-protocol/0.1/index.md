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
# <span data-ttu-id="0eedf-103">Notas de versão do protocolo DevTools versão 0,1</span><span class="sxs-lookup"><span data-stu-id="0eedf-103">DevTools Protocol Version 0.1 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="0eedf-104">O protocolo Microsoft Edge DevTools funciona apenas na [atualização de abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="0eedf-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="0eedf-105">A versão 0,1 do **protocolo Microsoft Edge devtools** fornece uma visualização antecipada para testar a instrumentação do EdgeHTML e a depuração remota básica no novo aplicativo autônomo do [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="0eedf-105">Version 0.1 of the Microsoft **Edge DevTools Protocol** provides an early preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="0eedf-106">Assim, requer que você execute a atualização do [Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) ou uma versão mais recente do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="0eedf-106">As such, it requires you to be running [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) or a later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) build.</span></span>

<span data-ttu-id="0eedf-107">As metas por trás do protocolo DevTools são de três dobras:</span><span class="sxs-lookup"><span data-stu-id="0eedf-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="0eedf-108">Fornecer uma API pública para o nosso aplicativo DevTools para anexar ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0eedf-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="0eedf-109">Expandir o acesso da funcionalidade do DevTools a clientes de ferramentas externos</span><span class="sxs-lookup"><span data-stu-id="0eedf-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="0eedf-110">Habilitar a depuração remota em todo o intervalo de dispositivos Windows 10 que executam o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0eedf-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="0eedf-111">Esta versão preliminar fornece a funcionalidade de depuração básica, como a configuração de pontos de interrupção, a depuração por meio do código e a exploração de rastreamentos de pilha.</span><span class="sxs-lookup"><span data-stu-id="0eedf-111">This preliminary release provides core debugging functionality, such as setting breakpoints, stepping through code, and exploring stack traces.</span></span> <span data-ttu-id="0eedf-112">Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis no painel do [**depurador**](../../devtools-guide/debugger.md) , subtração inspeção de cache (para armazenamento da Web, trabalho de serviço, API de cache e IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="0eedf-112">In the Edge DevTools UI, this translates to functionality available in the [**Debugger**](../../devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> 

<span data-ttu-id="0eedf-113">Outras funcionalidades do depurador serão adicionadas em versões futuras, seguidas da instrumentação religando outros painéis do [devtools](../index.md) .</span><span class="sxs-lookup"><span data-stu-id="0eedf-113">Further debugger functionality will be added in upcoming releases, followed by the instrumentation powering other [DevTools](../index.md) panels.</span></span>
