---
description: Tudo sobre melhorias do Serviço de Trabalho e como usar cada um deles.
title: Melhorias do Service Worker
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, service worker, PWA
ms.openlocfilehash: c00b7c7fd18d4bb3d413369ec1464c0cb0255311
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597141"
---
# <a name="service-worker-improvements"></a><span data-ttu-id="a1cc5-104">Melhorias do Service Worker</span><span class="sxs-lookup"><span data-stu-id="a1cc5-104">Service Worker improvements</span></span>  

<span data-ttu-id="a1cc5-105">Este artigo ensina sobre melhorias nas [][MdnServiceWorkerApi] ferramentas de desenvolvedor para trabalhar com funcionários de serviço e as solicitações de rede que passam por cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-105">This article teaches you about improvements to developer tools for working with [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="a1cc5-106">As **melhorias dos funcionários de** serviço estão nas **ferramentas Rede,** **Aplicativo** **e Fontes.**</span><span class="sxs-lookup"><span data-stu-id="a1cc5-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="a1cc5-107">As melhorias simplificam as tarefas a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-107">The improvements simplify the following tasks.</span></span>  

*   <span data-ttu-id="a1cc5-108">Depuração com base nas linhas do tempo do Trabalhador do Serviço.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="a1cc5-109">O início de uma solicitação e a duração da inicialização.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="a1cc5-110">Atualizar para o registro do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="a1cc5-111">O tempo de execução de uma solicitação usando o [manipulador de eventos de busca.][MdnFetchEvent]</span><span class="sxs-lookup"><span data-stu-id="a1cc5-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="a1cc5-112">O tempo de execução de todos os eventos de busca para carregar um cliente.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="a1cc5-113">Explore os detalhes do tempo de execução de manipuladores de eventos de busca, instale manipuladores de eventos e ative manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="a1cc5-114">Entrar e sair do manipulador de eventos de busca com informações [de script de página.](#sources)</span><span class="sxs-lookup"><span data-stu-id="a1cc5-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  
    
<span data-ttu-id="a1cc5-115">As experiências abrangem três ferramentas de desenvolvedor diferentes.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="a1cc5-116">A [ferramenta Rede.](#network)</span><span class="sxs-lookup"><span data-stu-id="a1cc5-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="a1cc5-117">Escolha uma solicitação de rede que seja executado por um trabalhador do serviço e acesse a linha do tempo correspondente do trabalhador do serviço na **ferramenta Timing.**</span><span class="sxs-lookup"><span data-stu-id="a1cc5-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="a1cc5-118">A [ferramenta Application.](#application)</span><span class="sxs-lookup"><span data-stu-id="a1cc5-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="a1cc5-119">Para depurar os funcionários do serviço, navegue até a **ferramenta Trabalhadores do** Serviço.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="a1cc5-120">A [ferramenta Sources.](#sources)</span><span class="sxs-lookup"><span data-stu-id="a1cc5-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="a1cc5-121">Acessar informações de script de página ao entrar em busca de manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-121">Access page script information when stepping into fetch event handlers.</span></span>  
    
## <a name="network"></a><span data-ttu-id="a1cc5-122">Rede</span><span class="sxs-lookup"><span data-stu-id="a1cc5-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Linha do tempo do trabalho de serviço na ferramenta Rede" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="a1cc5-124">Exibição de rede</span><span class="sxs-lookup"><span data-stu-id="a1cc5-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="a1cc5-125">Para acessar os recursos de depuração de funcionários de serviço na **ferramenta Rede,** conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="a1cc5-126">Acesse diretamente na **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="a1cc5-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="a1cc5-127">Iniciado na ferramenta **Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="a1cc5-127">Started in the **Application** tool.</span></span>  
    
### <a name="request-routing"></a><span data-ttu-id="a1cc5-128">Roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="a1cc5-128">Request routing</span></span>  

<span data-ttu-id="a1cc5-129">Para facilitar a visualização do roteamento de solicitações, os cronogramas agora exibem a start-up do serviço de trabalho e os `respondWith` eventos de busca.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="a1cc5-130">Para depurar e visualizar uma solicitação de rede que passou por um funcionário do serviço, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="a1cc5-131">Escolha a solicitação de rede que passou por um trabalhador de serviço.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="a1cc5-132">Abra a **ferramenta Timing.**</span><span class="sxs-lookup"><span data-stu-id="a1cc5-132">Open the **Timing** tool.</span></span>  
    
### <a name="fetch-events"></a><span data-ttu-id="a1cc5-133">Buscar eventos</span><span class="sxs-lookup"><span data-stu-id="a1cc5-133">Fetch events</span></span>  

<span data-ttu-id="a1cc5-134">Para saber mais sobre os eventos de busca, escolha a seta `respondWith` listada à esquerda do `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="a1cc5-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="a1cc5-135">Para encontrar mais detalhes sobre a **Solicitação Original** **e Resposta Recebida,** use as setas listadas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <a name="application"></a><span data-ttu-id="a1cc5-136">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a1cc5-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Exibição de aplicativo" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="a1cc5-138">Exibição de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a1cc5-138">Application view</span></span>  
:::image-end:::  

### <a name="service-worker-update-timeline"></a><span data-ttu-id="a1cc5-139">Linha do tempo de atualização do trabalhador do serviço</span><span class="sxs-lookup"><span data-stu-id="a1cc5-139">Service worker update timeline</span></span>  

<span data-ttu-id="a1cc5-140">A Microsoft Edge DevTools adicionou uma linha do tempo na ferramenta **Application** para refletir o ciclo de vida da atualização do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="a1cc5-141">Ele exibe os eventos de instalação e ativação.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="a1cc5-142">Cada um dos eventos tem uma seta de menu suspenso correspondente para dar mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <a name="request-routing-and-fetch-events"></a><span data-ttu-id="a1cc5-143">Solicitar eventos de roteamento e busca</span><span class="sxs-lookup"><span data-stu-id="a1cc5-143">Request routing and fetch events</span></span>  

<span data-ttu-id="a1cc5-144">Agora você pode acessar as linhas do tempo de trabalho do serviço por meio **da ferramenta Rede** na gaveta do console.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="a1cc5-145">O recurso beneficia o desempenho, minimiza a duplicação da interface do usuário e cria uma experiência de depuração mais abrangente.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="a1cc5-146">Abra o serviço que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="a1cc5-147">Escolha o **botão Rede** para abrir a experiência [de roteamento de solicitação](#network).</span><span class="sxs-lookup"><span data-stu-id="a1cc5-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="a1cc5-148">Use os **menus suspensos respondWith** para buscar informações de solicitação de evento e resposta.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="a1cc5-149">A **ferramenta Rede** exibe as solicitações de rede que passaram pelo trabalhador do serviço que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="a1cc5-150">O filtro automático é uma maneira de restringir sua exploração.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <a name="sources"></a><span data-ttu-id="a1cc5-151">Fontes</span><span class="sxs-lookup"><span data-stu-id="a1cc5-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Árvore DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="a1cc5-153">Árvore DOM</span><span class="sxs-lookup"><span data-stu-id="a1cc5-153">DOM tree</span></span>  
:::image-end:::  

<span data-ttu-id="a1cc5-154">Para encontrar mais informações de pilha, de definir um ponto de quebra no manipulador de busca.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="a1cc5-155">Os detalhes levam a onde o recurso é solicitado no script da página.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="a1cc5-156">Quando o depurador pausa dentro de um manipulador de busca, uma informação de pilha combinada é exibida no painel à direita.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="a1cc5-157">Depois disso, você pode se mover nos quadros de pilha.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-157">After that, you may move around in the stack frames.</span></span>  

### <a name="future-work"></a><span data-ttu-id="a1cc5-158">Trabalho futuro</span><span class="sxs-lookup"><span data-stu-id="a1cc5-158">Future work</span></span>  

<span data-ttu-id="a1cc5-159">A Microsoft Edge equipe do DevTools planeja desenvolver ainda mais os detalhes do cache e está investigando mais maneiras de melhorar a experiência de depuração de funcionários do serviço para desenvolvedores de [Aplicativo Web][MdnProgressiveWebApps] Progressivo.</span><span class="sxs-lookup"><span data-stu-id="a1cc5-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a1cc5-160">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a1cc5-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicativos Web progressivos (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de Trabalho de Serviço | MDN"  
