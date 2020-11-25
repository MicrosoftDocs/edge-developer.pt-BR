---
description: Tudo sobre os aprimoramentos do trabalho do serviço e como usar cada um deles.
title: Melhorias do trabalho do serviço
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, trabalhador do serviço, PWA
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190019"
---
# <span data-ttu-id="c6111-104">Melhorias do trabalho do serviço</span><span class="sxs-lookup"><span data-stu-id="c6111-104">Service Worker improvements</span></span>  

<span data-ttu-id="c6111-105">Este artigo ensina melhorias para os [funcionários do serviço][MdnServiceWorkerApi] e as solicitações de rede que passam por cada um deles.</span><span class="sxs-lookup"><span data-stu-id="c6111-105">This article teaches you about improvements to [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="c6111-106">As **melhorias de trabalho do serviço** estão nas ferramentas de **rede**, **aplicativo**e **fontes** .</span><span class="sxs-lookup"><span data-stu-id="c6111-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="c6111-107">Os aprimoramentos incluem as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="c6111-107">The improvements include the following tasks.</span></span>  

*   <span data-ttu-id="c6111-108">Depuração com base em cronogramas do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="c6111-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="c6111-109">O início de uma solicitação e duração da inicialização.</span><span class="sxs-lookup"><span data-stu-id="c6111-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="c6111-110">Atualize para o registro de trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="c6111-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="c6111-111">O tempo de execução de uma solicitação usando o manipulador de [eventos FETCH][MdnFetchEvent] .</span><span class="sxs-lookup"><span data-stu-id="c6111-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="c6111-112">O tempo de execução de todos os eventos de busca para carregar um cliente.</span><span class="sxs-lookup"><span data-stu-id="c6111-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="c6111-113">Explore os detalhes do tempo de execução de busca de manipuladores de eventos, instale manipuladores de eventos e ative manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="c6111-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="c6111-114">Depuração dentro e fora do manipulador de eventos FETCH com [informações de script de página](#sources).</span><span class="sxs-lookup"><span data-stu-id="c6111-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  

<span data-ttu-id="c6111-115">As experiências se estendem por três ferramentas de desenvolvedor diferentes.</span><span class="sxs-lookup"><span data-stu-id="c6111-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="c6111-116">A ferramenta [rede](#network) .</span><span class="sxs-lookup"><span data-stu-id="c6111-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="c6111-117">Escolha uma solicitação de rede que seja executada por meio de um trabalhador de serviço e acesse a linha do tempo correspondente do trabalho de serviço na ferramenta de **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="c6111-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="c6111-118">A ferramenta do [aplicativo](#application) .</span><span class="sxs-lookup"><span data-stu-id="c6111-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="c6111-119">Para depurar os trabalhadores do serviço, navegue até a ferramenta **trabalhadores do serviço** .</span><span class="sxs-lookup"><span data-stu-id="c6111-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="c6111-120">A ferramenta [fontes](#sources) .</span><span class="sxs-lookup"><span data-stu-id="c6111-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="c6111-121">Acessar informações de script de página ao entrar em busca de manipuladores de eventos de busca.</span><span class="sxs-lookup"><span data-stu-id="c6111-121">Access page script information when stepping into fetch event handlers.</span></span>  

## <span data-ttu-id="c6111-122">Rede</span><span class="sxs-lookup"><span data-stu-id="c6111-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Linha do tempo de trabalho do serviço na ferramenta de rede" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="c6111-124">Tela de rede</span><span class="sxs-lookup"><span data-stu-id="c6111-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="c6111-125">Para acessar os recursos de depuração de trabalho do serviço na ferramenta **rede** , execute uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="c6111-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="c6111-126">Acesse diretamente na ferramenta **rede** .</span><span class="sxs-lookup"><span data-stu-id="c6111-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="c6111-127">Iniciou na ferramenta do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="c6111-127">Started in the **Application** tool.</span></span>  
    
### <span data-ttu-id="c6111-128">Roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="c6111-128">Request routing</span></span>  

<span data-ttu-id="c6111-129">Para facilitar a visualização do roteamento de solicitação, os cronogramas agora exibem os eventos de início e busca do trabalho do serviço `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="c6111-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="c6111-130">Para depurar e visualizar uma solicitação de rede transmitida por meio de um trabalhador de serviço, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6111-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="c6111-131">Escolha a solicitação de rede que passou por um trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="c6111-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="c6111-132">Abrir a ferramenta de **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="c6111-132">Open the **Timing** tool.</span></span>  
    
### <span data-ttu-id="c6111-133">Buscar eventos</span><span class="sxs-lookup"><span data-stu-id="c6111-133">Fetch events</span></span>  

<span data-ttu-id="c6111-134">Para saber mais sobre os `respondWith` eventos de busca, escolha a seta suspensa à esquerda do `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="c6111-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="c6111-135">Para saber mais detalhes sobre a **solicitação** e a **resposta originais recebidas**, use as setas suspensas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c6111-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <span data-ttu-id="c6111-136">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6111-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Visualização do aplicativo" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="c6111-138">Visualização do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6111-138">Application view</span></span>  
:::image-end:::  

### <span data-ttu-id="c6111-139">Linha do tempo de atualização de trabalho do serviço</span><span class="sxs-lookup"><span data-stu-id="c6111-139">Service worker update timeline</span></span>  

<span data-ttu-id="c6111-140">A equipe do Microsoft Edge DevTools adicionou uma linha do tempo na ferramenta do **aplicativo** para refletir o ciclo de vida de atualização do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="c6111-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="c6111-141">Ele exibe os eventos de instalação e ativação.</span><span class="sxs-lookup"><span data-stu-id="c6111-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="c6111-142">Cada um dos eventos tem uma seta suspensa correspondente para fornecer mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="c6111-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <span data-ttu-id="c6111-143">Eventos de roteamento e busca de solicitação</span><span class="sxs-lookup"><span data-stu-id="c6111-143">Request routing and fetch events</span></span>  

<span data-ttu-id="c6111-144">Agora você pode acessar o cronograma do trabalhador do serviço por meio da ferramenta **rede** na gaveta do console.</span><span class="sxs-lookup"><span data-stu-id="c6111-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="c6111-145">O recurso beneficia o desempenho, minimiza a duplicação da interface do usuário e cria uma experiência de depuração mais abrangente.</span><span class="sxs-lookup"><span data-stu-id="c6111-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="c6111-146">Abra o trabalhador do serviço que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="c6111-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="c6111-147">Escolha o botão **rede** para abrir a [experiência de roteamento de solicitações](#network).</span><span class="sxs-lookup"><span data-stu-id="c6111-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="c6111-148">Use os dropdowns **respondWith** para obter informações de solicitação e resposta de eventos.</span><span class="sxs-lookup"><span data-stu-id="c6111-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="c6111-149">A ferramenta **rede** exibe as solicitações de rede que passaram pelo trabalhador do serviço que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="c6111-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="c6111-150">O filtro automático é uma maneira de restringir a exploração.</span><span class="sxs-lookup"><span data-stu-id="c6111-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <span data-ttu-id="c6111-151">Fontes</span><span class="sxs-lookup"><span data-stu-id="c6111-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Modo de exibição DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="c6111-153">Modo de exibição DOM</span><span class="sxs-lookup"><span data-stu-id="c6111-153">DOM view</span></span>  
:::image-end:::  

<span data-ttu-id="c6111-154">Para encontrar mais informações sobre pilha, defina um ponto de interrupção no manipulador de busca.</span><span class="sxs-lookup"><span data-stu-id="c6111-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="c6111-155">Os detalhes resultam no local em que o recurso é solicitado no script de página.</span><span class="sxs-lookup"><span data-stu-id="c6111-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="c6111-156">Quando o depurador pausar dentro de um manipulador de busca, as informações de pilha combinadas serão exibidas no painel à direita.</span><span class="sxs-lookup"><span data-stu-id="c6111-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="c6111-157">Depois disso, você pode percorrer os quadros de pilha.</span><span class="sxs-lookup"><span data-stu-id="c6111-157">After that, you may move around in the stack frames.</span></span>  

### <span data-ttu-id="c6111-158">Trabalho futuro</span><span class="sxs-lookup"><span data-stu-id="c6111-158">Future work</span></span>  

<span data-ttu-id="c6111-159">A equipe Microsoft Edge DevTools planeja mais desenvolver o detalhe do cache e está investigando mais maneiras de melhorar a experiência de depuração do trabalho do serviço para desenvolvedores de [aplicativos Web progressivos][MdnProgressiveWebApps] .</span><span class="sxs-lookup"><span data-stu-id="c6111-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <span data-ttu-id="c6111-160">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c6111-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicativos Web progressivos (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabalho do serviço | MDN"  
