---
description: Modelo de processo
title: Modelo de processo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895531"
---
# <span data-ttu-id="a6687-104">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="a6687-104">Process model</span></span>  

<span data-ttu-id="a6687-105">O WebView2 usa o mesmo modelo de processo do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a6687-105">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="a6687-106">Para obter mais informações sobre o modelo de processo do navegador, consulte [arquitetura do navegador – examine o navegador da Web moderno][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span><span class="sxs-lookup"><span data-stu-id="a6687-106">For more information about the browser process model, see [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span> 

<span data-ttu-id="a6687-107">Um processo do navegador está associado aos processos do renderizador e outros processos do utilitário conforme descrito nesse artigo.</span><span class="sxs-lookup"><span data-stu-id="a6687-107">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="a6687-108">Além disso, no caso do WebView2, há um aplicativo host solicitando processos usando WebView2.</span><span class="sxs-lookup"><span data-stu-id="a6687-108">Additionally, in the case of WebView2, there are host app requesting processes using WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processo 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="a6687-110">Processo 1</span><span class="sxs-lookup"><span data-stu-id="a6687-110">Process 1</span></span>  
:::image-end:::  

<span data-ttu-id="a6687-111">Um processo do navegador é especificado na pasta dados do usuário em uma sessão do usuário que atende a qualquer WebView2 que solicita o processo que especifica a pasta dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6687-111">One browser process is specified per user data folder in a user session that serve any WebView2 requesting process that specifies that user data folder.</span></span>  <span data-ttu-id="a6687-112">Isso significa que um processo de navegador pode estar servindo vários processos de solicitação e um processo de solicitação pode estar usando vários processos do navegador.</span><span class="sxs-lookup"><span data-stu-id="a6687-112">This means one browser process may be serving multiple requesting processes and one requesting process may be using multiple browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processo 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="a6687-114">Processo 2</span><span class="sxs-lookup"><span data-stu-id="a6687-114">Process 2</span></span>  
:::image-end:::  

<span data-ttu-id="a6687-115">Um processo de navegador tem alguns processos de renderização associados.</span><span class="sxs-lookup"><span data-stu-id="a6687-115">A browser process has some number of associated renderer processes.</span></span>  <span data-ttu-id="a6687-116">Os processos do navegador são criados conforme necessário para atender a potencialmente vários quadros em diferentes instâncias do WebView2.</span><span class="sxs-lookup"><span data-stu-id="a6687-116">The browser processes are created as required to service potentially multiple frames in different instances of WebView2.</span></span>  <span data-ttu-id="a6687-117">O número de processos de renderização varia de acordo com o recurso de navegador de isolamento de site e o número de origens discadas discadas renderizadas em instâncias associadas do WebView2.</span><span class="sxs-lookup"><span data-stu-id="a6687-117">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  <span data-ttu-id="a6687-118">O recurso de navegador de isolamento de site é descrito no conteúdo anterior.</span><span class="sxs-lookup"><span data-stu-id="a6687-118">The site isolation browser feature is described in the previous content.</span></span>  

<span data-ttu-id="a6687-119">O `CoreWebView2Environment` representa um processo de navegador e pasta de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6687-119">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="a6687-120">O `CoreWebView2` não corresponde diretamente a qualquer conjunto de processos, pois vários processos de renderização são usados por um WebView2 dependendo do isolamento do site conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a6687-120">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on site isolation as previously described.</span></span>  

<span data-ttu-id="a6687-121">Você pode reagir a falhas e travamentos nesses processos de navegador e renderização usando o `ProcessFailed` evento de `CoreWebView2` .</span><span class="sxs-lookup"><span data-stu-id="a6687-121">You are able to react to crashes and hangs in these browser and renderer processes using the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="a6687-122">Você pode desligar com segurança os processos do navegador e do renderizador associados usando o `Close` método of `CoreWebView2Controller` .</span><span class="sxs-lookup"><span data-stu-id="a6687-122">You are able to safely shutdown associated browser and renderer processes using the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="a6687-123">Para abrir a janela do Gerenciador de tarefas do navegador da janela do **devtools** de uma instância do WebView2, você pode selecionar `Shift` + `Escape` ou passar o mouse na barra de título da janela do devtools, abrir o menu contextual \ (clique com o botão direito do mouse \) e escolher `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="a6687-123">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, you are able to select `Shift`+`Escape` or hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  <span data-ttu-id="a6687-124">Todos os processos associados ao processo do navegador de seu WebView2 são exibidos incluindo finalidades associadas.</span><span class="sxs-lookup"><span data-stu-id="a6687-124">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitetura do navegador – veja dentro do navegador da Web moderno (parte 1)"  
