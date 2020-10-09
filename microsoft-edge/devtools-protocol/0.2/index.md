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
# <span data-ttu-id="a5c0d-103">Notas de versão do protocolo DevTools versão 0,2</span><span class="sxs-lookup"><span data-stu-id="a5c0d-103">DevTools Protocol Version 0.2 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="a5c0d-104">A versão 0,2 do protocolo Microsoft Edge DevTools funciona apenas na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="a5c0d-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/getting-started/) builds.</span></span>

<span data-ttu-id="a5c0d-105">A versão 0,2 do **protocolo Microsoft Edge devtools** fornece uma visualização para testar a instrumentação do EdgeHTML e a depuração remota básica no novo aplicativo autônomo do [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="a5c0d-105">Version 0.2 of the Microsoft **Edge DevTools Protocol** provides a preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="a5c0d-106">Assim, requer que você execute a [atualização do Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) ou uma versão mais recente do [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="a5c0d-106">As such, it requires you to be running the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later [Windows Insider Preview](https://insider.windows.com/getting-started/) build.</span></span>

<span data-ttu-id="a5c0d-107">As metas por trás do protocolo DevTools são de três dobras:</span><span class="sxs-lookup"><span data-stu-id="a5c0d-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="a5c0d-108">Fornecer uma API pública para o nosso aplicativo DevTools para anexar ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5c0d-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="a5c0d-109">Expandir o acesso da funcionalidade do DevTools a clientes de ferramentas externos</span><span class="sxs-lookup"><span data-stu-id="a5c0d-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="a5c0d-110">Habilitar a depuração remota em todo o intervalo de dispositivos Windows 10 que executam o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5c0d-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="a5c0d-111">A versão 0,2 do protocolo DevTools inclui novos domínios para a depuração de estilo e o layout (somente leitura) e APIs de console, além da funcionalidade de depuração de script principal introduzida na versão 0,1.</span><span class="sxs-lookup"><span data-stu-id="a5c0d-111">Version 0.2 of the DevTools Protocol includes new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="a5c0d-112">Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis nos painéis de [**elementos**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) e [**depurador**](../../devtools-guide/debugger.md)  .</span><span class="sxs-lookup"><span data-stu-id="a5c0d-112">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md)  panels.</span></span>
