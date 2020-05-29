---
title: Guia de problemas de rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 018a6ef89242d55cefaa974641be456f4501c557
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611802"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="0f3e5-103">Guia de problemas de rede</span><span class="sxs-lookup"><span data-stu-id="0f3e5-103">Network Issues Guide</span></span>   




<span data-ttu-id="0f3e5-104">Este guia mostra como detectar problemas de rede ou oportunidades de otimização no painel rede do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="0f3e5-105">Consulte [introdução][NetworkPerformance] para aprender as noções básicas do painel rede.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-105">See [Get Started][NetworkPerformance] to learn the basics of the Network panel.</span></span>  

## <span data-ttu-id="0f3e5-106">Solicitações em fila ou interrompidas</span><span class="sxs-lookup"><span data-stu-id="0f3e5-106">Queued or stalled requests</span></span>   

### <span data-ttu-id="0f3e5-107">Sintomas</span><span class="sxs-lookup"><span data-stu-id="0f3e5-107">Symptoms</span></span>  

<span data-ttu-id="0f3e5-108">Seis solicitações estão sendo baixadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="0f3e5-109">Depois disso, uma série de solicitações é enfileirada ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="0f3e5-110">Após a conclusão de uma das primeiras seis solicitações, uma das solicitações na fila é iniciada.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="0f3e5-111">Na **cascata** na [Figura 1](#figure-1), as primeiras seis solicitações para o `edge-iconx1024.msft.png` ativo começam simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-111">In the **Waterfall** in [Figure 1](#figure-1), the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="0f3e5-112">As solicitações subsequentes serão interrompidas até que uma das 6 originais seja concluída.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

> ##### <span data-ttu-id="0f3e5-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="0f3e5-113">Figure 1</span></span>  
> <span data-ttu-id="0f3e5-114">Um exemplo de uma série em fila ou Stallion no painel rede</span><span class="sxs-lookup"><span data-stu-id="0f3e5-114">An example of a queued or stalled series in the Network panel</span></span>  
> ![Um exemplo de uma série em fila ou Stallion no painel rede][ImageStalled]  

### <span data-ttu-id="0f3e5-116">Causas</span><span class="sxs-lookup"><span data-stu-id="0f3e5-116">Causes</span></span>  

<span data-ttu-id="0f3e5-117">Muitas solicitações estão sendo feitas em um único domínio.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="0f3e5-118">Em conexões HTTP/1.0 ou HTTP/1.1, o Microsoft Edge permite um máximo de seis conexões TCP simultâneas por host.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

### <span data-ttu-id="0f3e5-119">Corrige</span><span class="sxs-lookup"><span data-stu-id="0f3e5-119">Fixes</span></span>  

*   <span data-ttu-id="0f3e5-120">Implemente o fragmentação de domínio se você precisar usar HTTP/1.0 ou HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="0f3e5-121">Use HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-121">Use HTTP/2.</span></span>  <span data-ttu-id="0f3e5-122">Não use o fragmentação de domínio com HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="0f3e5-123">Remova ou adie solicitações desnecessárias para que as solicitações críticas sejam baixadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  

## <span data-ttu-id="0f3e5-124">Tempo de demora para o primeiro byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="0f3e5-124">Slow Time To First Byte (TTFB)</span></span>   

### <span data-ttu-id="0f3e5-125">Sintomas</span><span class="sxs-lookup"><span data-stu-id="0f3e5-125">Symptoms</span></span>  

<span data-ttu-id="0f3e5-126">Uma solicitação gasta muito tempo esperando receber o primeiro byte do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="0f3e5-127">Na [Figura 2](#figure-2), a barra verde longa na **cascata** indica que a solicitação estava aguardando muito tempo.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-127">In [Figure 2](#figure-2), the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="0f3e5-128">Isso foi simulado usando um perfil para restringir a velocidade da rede e adicionar um atraso.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

> ##### <span data-ttu-id="0f3e5-129">Figura 2</span><span class="sxs-lookup"><span data-stu-id="0f3e5-129">Figure 2</span></span>  
> <span data-ttu-id="0f3e5-130">Um exemplo de uma solicitação com um tempo de demora para o primeiro byte</span><span class="sxs-lookup"><span data-stu-id="0f3e5-130">An example of a request with a slow Time To First Byte</span></span>  
> ![Um exemplo de uma solicitação com um tempo de demora para o primeiro byte][ImageSlowTimeToFirstByte]  

### <span data-ttu-id="0f3e5-132">Causas</span><span class="sxs-lookup"><span data-stu-id="0f3e5-132">Causes</span></span>  

*   <span data-ttu-id="0f3e5-133">A conexão entre o cliente e o servidor está lenta.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-133">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="0f3e5-134">O servidor está lento para responder.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-134">The server is slow to respond.</span></span>  <span data-ttu-id="0f3e5-135">Hospede o servidor localmente para determinar se ele é a conexão ou o servidor que está lento.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-135">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="0f3e5-136">Se você ainda receber um tempo lento para o primeiro byte \ (TTFB \) ao acessar um servidor local, então o servidor está lento.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-136">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  

### <span data-ttu-id="0f3e5-137">Corrige</span><span class="sxs-lookup"><span data-stu-id="0f3e5-137">Fixes</span></span>  

*   <span data-ttu-id="0f3e5-138">Se a conexão for lenta, considere hospedar o conteúdo em uma CDN ou alterar provedores de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-138">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="0f3e5-139">Se o servidor estiver lento, considere a otimização de consultas de banco de dados, a implementação de um cache ou a modificação da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-139">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  

## <span data-ttu-id="0f3e5-140">Download de conteúdo lento</span><span class="sxs-lookup"><span data-stu-id="0f3e5-140">Slow content download</span></span>   

### <span data-ttu-id="0f3e5-141">Sintomas</span><span class="sxs-lookup"><span data-stu-id="0f3e5-141">Symptoms</span></span>  

<span data-ttu-id="0f3e5-142">Uma solicitação demora muito tempo para baixar.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-142">A request takes a long time to download.</span></span>  

<span data-ttu-id="0f3e5-143">Na [Figura 3](#figure-3), a barra azul longa na **cascata** ao lado do png significa que demorou muito tempo para baixar.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-143">In [Figure 3](#figure-3), the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

> ##### <span data-ttu-id="0f3e5-144">Figura 3</span><span class="sxs-lookup"><span data-stu-id="0f3e5-144">Figure 3</span></span>  
> <span data-ttu-id="0f3e5-145">Um exemplo de uma solicitação que demora muito tempo para baixar</span><span class="sxs-lookup"><span data-stu-id="0f3e5-145">An example of a request that takes a long time to download</span></span>  
> ![Um exemplo de uma solicitação que demora muito tempo para baixar][ImageSlowContentDownload]  

### <span data-ttu-id="0f3e5-147">Causas</span><span class="sxs-lookup"><span data-stu-id="0f3e5-147">Causes</span></span>  

*   <span data-ttu-id="0f3e5-148">A conexão entre o cliente e o servidor está lenta.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-148">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="0f3e5-149">Uma grande quantidade de conteúdo está sendo baixada.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-149">A lot of content is being downloaded.</span></span>  

### <span data-ttu-id="0f3e5-150">Corrige</span><span class="sxs-lookup"><span data-stu-id="0f3e5-150">Fixes</span></span>  

*   <span data-ttu-id="0f3e5-151">Considere hospedar o conteúdo em uma CDN ou alterar provedores de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-151">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="0f3e5-152">Envie menos bytes otimizando suas solicitações.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-152">Send fewer bytes by optimizing your requests.</span></span>  

## <span data-ttu-id="0f3e5-153">Conhecimento do Contribute</span><span class="sxs-lookup"><span data-stu-id="0f3e5-153">Contribute knowledge</span></span>  

<span data-ttu-id="0f3e5-154">Você tem um problema de rede que deve ser adicionado a este guia?</span><span class="sxs-lookup"><span data-stu-id="0f3e5-154">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="0f3e5-155">Envie um tweet para [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="0f3e5-155">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="0f3e5-156">Selecione **enviar comentários** ![ enviar comentários ][ImageSendFeedbackIcon] no devtools ou pressione `Alt` + `Shift` + `I` \ (Windows \) ou `Option` + `Shift` + `I` \ (MacOS \) para fornecer comentários ou solicitações de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-156">Select **Send Feedback** ![Send Feedback][ImageSendFeedbackIcon] in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="0f3e5-157">[Abra um problema][WebFundamentalsIssue] no repositório de documentos.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-157">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  

<!--   -->  



<!-- image links -->  

[ImageSendFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/smile-icon.msft.png  

[ImageStalled]: /microsoft-edge/devtools-guide-chromium/media/network-network-disabled-cache-resources-queue.msft.png "Figura 1: um exemplo de uma série enfileirada ou Stallion no painel de rede"  
[ImageSlowTimeToFirstByte]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-using-dial-up-profile.msft.png "Figura 2: um exemplo de uma solicitação com um tempo de demora para o primeiro byte"  
[ImageSlowContentDownload]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-edge-devtools.msft.png "Figura 3: um exemplo de uma solicitação que demora muito tempo para baixar"  

<!-- links -->  

[NetworkPerformance]: /microsoft-edge/devtools-guide-chromium/network/index "Inspecionar atividades de rede no Microsoft Edge DevTools"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Novo problema-MicrosoftDocs/Edge-Developer"  

> [!NOTE]
> <span data-ttu-id="0f3e5-163">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="0f3e5-163">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0f3e5-164">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/issues) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Jonathan Garbee][JonathanGarbee] \ (Google Developer expert para tecnologia da Web \).</span><span class="sxs-lookup"><span data-stu-id="0f3e5-164">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0f3e5-166">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0f3e5-166">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
