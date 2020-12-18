---
description: Veja o que há de novo no Microsoft Edge DevTools na atualização de outubro de 2018 do Windows 10 de outubro
title: O que há de novo no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1d3c6fe5bf061186d5c6593a115a8b6794c0dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231707"
---
# <span data-ttu-id="e4614-104">DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)</span><span class="sxs-lookup"><span data-stu-id="e4614-104">DevTools in the latest Windows 10 update (EdgeHTML 18)</span></span>

<span data-ttu-id="e4614-105">A atualização mais recente do Microsoft Edge DevTools adiciona uma série de conveniências à interface do usuário e nos bastidores, incluindo novos painéis dedicados [*para trabalhadores de serviço*](#service-workers-panel) e [*armazenamento*](#storage-panel), ferramentas de pesquisa de [arquivos](#source-file-search-tools) de origem no depurador e novos domínios de [protocolo de devtools](#edge-devtools-protocol-updates) para a depuração de estilo/layout e APIs do console.</span><span class="sxs-lookup"><span data-stu-id="e4614-105">The latest update to Microsoft Edge DevTools adds a number of conveniences both to the UI and under the hood, including new dedicated panels for [*Service Workers*](#service-workers-panel) and [*Storage*](#storage-panel), source [file search](#source-file-search-tools) tools in the Debugger, and new [Edge DevTools Protocol domains](#edge-devtools-protocol-updates) for style/layout debugging and console APIs.</span></span>

<span data-ttu-id="e4614-106">Estes são os recursos mais recentes do Microsoft Edge DevTools disponíveis agora na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span><span class="sxs-lookup"><span data-stu-id="e4614-106">Here are the latest Microsoft Edge DevTools features available now in the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span></span> <span data-ttu-id="e4614-107">Além de tudo isso, também corrigimos vários bugs de acessibilidade, confiabilidade e desempenho para melhorar os conceitos básicos!</span><span class="sxs-lookup"><span data-stu-id="e4614-107">In addition to all this, we’ve also fixed a number of accessibility, reliability, and performance bugs to improve fundamentals!</span></span>

## <span data-ttu-id="e4614-108">Aplicativo DevTools</span><span class="sxs-lookup"><span data-stu-id="e4614-108">DevTools app</span></span>

<span data-ttu-id="e4614-109">Atualizamos o aplicativo autônomo [Microsoft Edge devtools Preview](./index.md#microsoft-store-app).</span><span class="sxs-lookup"><span data-stu-id="e4614-109">We've updated the standalone [Microsoft Edge DevTools Preview app](./index.md#microsoft-store-app).</span></span> <span data-ttu-id="e4614-110">A versão mais recente inclui acesso remoto à depuração para funtionality núcleo no [**depurador**](./debugger.md), [**elementos**](./elements.md) (para operações somente leitura) e painéis do [**console**](./console.md) .</span><span class="sxs-lookup"><span data-stu-id="e4614-110">The latest release includes remote debugging access to core funtionality in the [**Debugger**](./debugger.md), [**Elements**](./elements.md) (for read-only operations), and [**Console**](./console.md) panels.</span></span>

## <span data-ttu-id="e4614-111">Painel funcionários do serviço</span><span class="sxs-lookup"><span data-stu-id="e4614-111">Service Workers panel</span></span>

<span data-ttu-id="e4614-112">Agora há um painel de [**funcionários**](./service-workers.md) dedicado para inspecionar, gerenciar e depurar os funcionários de serviço do seu site.</span><span class="sxs-lookup"><span data-stu-id="e4614-112">There's now a dedicated [**Service Workers**](./service-workers.md) panel for inspecting, managing, and debugging your site's service workers.</span></span> <span data-ttu-id="e4614-113">Isso fornece a mesma funcionalidade que anteriormente estava no painel do *depurador* (agora com uma interface do usuário menos cheia!).</span><span class="sxs-lookup"><span data-stu-id="e4614-113">This provides the same functionality as was previously in the *Debugger* panel (now with a less-crowded UI!).</span></span>

![Painel funcionários do serviço](./media/service_worker.png)

## <span data-ttu-id="e4614-115">Painel de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e4614-115">Storage panel</span></span>

<span data-ttu-id="e4614-116">Também mudamos todos os inspetores de armazenamento local (*armazenamento local e sesion, IndexedDB, cookies, cache*) anteriormente no *depurador* para o próprio painel de [**armazenamento**](./storage.md) exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e4614-116">We've also moved all the local storage inspectors (*Local and Sesion Storage, IndexedDB, Cookies, Cache*) previously in the *Debugger* to their own dedicated [**Storage**](./storage.md) panel.</span></span>

![Painel de armazenamento](./media/storage_cache.png)

## <span data-ttu-id="e4614-118">Ferramentas de pesquisa de arquivos de origem</span><span class="sxs-lookup"><span data-stu-id="e4614-118">Source file search tools</span></span>

<span data-ttu-id="e4614-119">O [**depurador**](./debugger.md) agora tem um painel de [pesquisa de arquivo de origem](./debugger.md#file-search) .</span><span class="sxs-lookup"><span data-stu-id="e4614-119">The [**Debugger**](./debugger.md) now has a [source file search](./debugger.md#file-search) pane.</span></span> <span data-ttu-id="e4614-120">Abra-o com o comando *Find in Files* ( `Ctrl` + `Shift` + `F` ) quando você tiver uma cadeia de caracteres específica de código que você está tentando encontrar na fonte.</span><span class="sxs-lookup"><span data-stu-id="e4614-120">Open it with the *Find in files* command (`Ctrl`+`Shift`+`F`) when you have a specific string of code you're trying to find in the source.</span></span> <span data-ttu-id="e4614-121">A barra de ferramentas fornece opções de pesquisa diferentes, incluindo expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="e4614-121">The toolbar provides different search options, including regular expressions.</span></span> 

![Pesquisa de arquivos do depurador](./media/debugger_file_search.png)

<span data-ttu-id="e4614-123">Você também pode abrir rapidamente qualquer arquivo de origem carregado com o comando *Abrir arquivo* ( `Ctrl` + `P` ).</span><span class="sxs-lookup"><span data-stu-id="e4614-123">You can also quickly open any loaded source file with the *Open file* (`Ctrl`+`P`) command.</span></span>

![Arquivo aberto do depurador](./media/debugger_open_file.png)

## <span data-ttu-id="e4614-125">Atualizações do protocolo Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e4614-125">Edge DevTools Protocol updates</span></span>

<span data-ttu-id="e4614-126">A [versão 0,2](../devtools-protocol/0.2/index.md) do protocolo devtools fornece novos domínios para a depuração de estilo e o layout (somente leitura) e APIs de console, além da funcionalidade de depuração de script principal introduzida na [versão 0,1](../devtools-protocol/0.1/index.md).</span><span class="sxs-lookup"><span data-stu-id="e4614-126">[Version 0.2](../devtools-protocol/0.2/index.md) of the DevTools Protocol provides new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in [Version 0.1](../devtools-protocol/0.1/index.md).</span></span> <span data-ttu-id="e4614-127">Na interface do usuário de borda DevTools, isso se traduz na funcionalidade disponível nos [**elementos**](../devtools-guide/elements.md) (para operações somente leitura), [**console**](../devtools-guide/console.md) e painéis do [**depurador**](../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="e4614-127">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../devtools-guide/elements.md) (for read-only operations), [**Console**](../devtools-guide/console.md) and [**Debugger**](../devtools-guide/debugger.md) panels.</span></span>
