---
description: Notas de versão para o protocolo Microsoft Edge DevTools versão 0,2
title: Notas de versão do protocolo Microsoft Edge DevTools versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 61d8f5b00dca3505594ca41db6c80c5ba4157092
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231296"
---
# <span data-ttu-id="3674b-103">Notas de versão do protocolo DevTools versão 0,2</span><span class="sxs-lookup"><span data-stu-id="3674b-103">DevTools Protocol Version 0.2 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="3674b-104">A versão 0,2 do protocolo Microsoft Edge DevTools funciona apenas na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="3674b-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/getting-started/) builds.</span></span>

<span data-ttu-id="3674b-105">A versão 0,2 do **protocolo Microsoft Edge devtools** fornece uma visualização para testar a instrumentação do EdgeHTML e a depuração remota básica no novo aplicativo autônomo do [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="3674b-105">Version 0.2 of the Microsoft **Edge DevTools Protocol** provides a preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="3674b-106">Assim, requer que você execute a [atualização do Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) ou uma versão mais recente do [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="3674b-106">As such, it requires you to be running the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later [Windows Insider Preview](https://insider.windows.com/getting-started/) build.</span></span>

<span data-ttu-id="3674b-107">As metas por trás do protocolo DevTools são de três dobras:</span><span class="sxs-lookup"><span data-stu-id="3674b-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="3674b-108">Fornecer uma API pública para o nosso aplicativo DevTools para anexar ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3674b-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="3674b-109">Expandir o acesso da funcionalidade do DevTools a clientes de ferramentas externos</span><span class="sxs-lookup"><span data-stu-id="3674b-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="3674b-110">Habilitar a depuração remota em todo o intervalo de dispositivos Windows 10 que executam o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3674b-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="3674b-111">A versão 0,2 do protocolo DevTools inclui novos domínios para a depuração de estilo e o layout (somente leitura) e APIs de console, além da funcionalidade de depuração de script principal introduzida na versão 0,1.</span><span class="sxs-lookup"><span data-stu-id="3674b-111">Version 0.2 of the DevTools Protocol includes new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="3674b-112">Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis nos painéis de [**elementos**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) e [**depurador**](../../devtools-guide/debugger.md)  .</span><span class="sxs-lookup"><span data-stu-id="3674b-112">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md)  panels.</span></span>
