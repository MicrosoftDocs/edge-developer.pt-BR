---
title: Guia de Problemas de Rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a9a3234f3516bef16328102858363ffcb06251ec
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985369"
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





# <span data-ttu-id="21514-103">Guia de problemas de rede</span><span class="sxs-lookup"><span data-stu-id="21514-103">Network issues guide</span></span>   




<span data-ttu-id="21514-104">Este guia mostra como detectar problemas de rede ou oportunidades de otimização no painel rede do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="21514-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="21514-105">Consulte [introdução][NetworkPerformance] para aprender as noções básicas do painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="21514-105">See [Get Started][NetworkPerformance] to learn the basics of the **Network** panel.</span></span>  

## <span data-ttu-id="21514-106">Solicitações em fila ou interrompidas</span><span class="sxs-lookup"><span data-stu-id="21514-106">Queued or stalled requests</span></span>   

**<span data-ttu-id="21514-107">Sintomas</span><span class="sxs-lookup"><span data-stu-id="21514-107">Symptoms</span></span>**  

<span data-ttu-id="21514-108">Seis solicitações estão sendo baixadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="21514-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="21514-109">Depois disso, uma série de solicitações é enfileirada ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="21514-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="21514-110">Após a conclusão de uma das primeiras seis solicitações, uma das solicitações na fila é iniciada.</span><span class="sxs-lookup"><span data-stu-id="21514-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="21514-111">Na **cascata** na figura a seguir, as primeiras seis solicitações para o `edge-iconx1024.msft.png` ativo começam simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="21514-111">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="21514-112">As solicitações subsequentes serão interrompidas até que uma das 6 originais seja concluída.</span><span class="sxs-lookup"><span data-stu-id="21514-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Um exemplo de uma série em fila ou Stallion no painel rede" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="21514-114">Um exemplo de uma série em fila ou Stallion no painel **rede**</span><span class="sxs-lookup"><span data-stu-id="21514-114">An example of a queued or stalled series in the **Network** panel</span></span>  
:::image-end:::  

**<span data-ttu-id="21514-115">Causas</span><span class="sxs-lookup"><span data-stu-id="21514-115">Causes</span></span>**  

<span data-ttu-id="21514-116">Muitas solicitações estão sendo feitas em um único domínio.</span><span class="sxs-lookup"><span data-stu-id="21514-116">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="21514-117">Em conexões HTTP/1.0 ou HTTP/1.1, o Microsoft Edge permite um máximo de seis conexões TCP simultâneas por host.</span><span class="sxs-lookup"><span data-stu-id="21514-117">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="21514-118">Corrige</span><span class="sxs-lookup"><span data-stu-id="21514-118">Fixes</span></span>**  

*   <span data-ttu-id="21514-119">Implemente o fragmentação de domínio se você precisar usar HTTP/1.0 ou HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="21514-119">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="21514-120">Use HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="21514-120">Use HTTP/2.</span></span>  <span data-ttu-id="21514-121">Não use o fragmentação de domínio com HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="21514-121">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="21514-122">Remova ou adie solicitações desnecessárias para que as solicitações críticas sejam baixadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="21514-122">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <span data-ttu-id="21514-123">Tempo de demora para o primeiro byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="21514-123">Slow Time To First Byte (TTFB)</span></span>   

**<span data-ttu-id="21514-124">Sintomas</span><span class="sxs-lookup"><span data-stu-id="21514-124">Symptoms</span></span>**  

<span data-ttu-id="21514-125">Uma solicitação gasta muito tempo esperando receber o primeiro byte do servidor.</span><span class="sxs-lookup"><span data-stu-id="21514-125">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="21514-126">Na figura a seguir, o longo, a barra verde na **cascata** indica que a solicitação estava aguardando muito tempo.</span><span class="sxs-lookup"><span data-stu-id="21514-126">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="21514-127">Isso foi simulado usando um perfil para restringir a velocidade da rede e adicionar um atraso.</span><span class="sxs-lookup"><span data-stu-id="21514-127">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Um exemplo de uma solicitação com um tempo de demora para o primeiro byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="21514-129">Um exemplo de uma solicitação com um tempo de demora para o primeiro byte</span><span class="sxs-lookup"><span data-stu-id="21514-129">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="21514-130">Causas</span><span class="sxs-lookup"><span data-stu-id="21514-130">Causes</span></span>**  

*   <span data-ttu-id="21514-131">A conexão entre o cliente e o servidor está lenta.</span><span class="sxs-lookup"><span data-stu-id="21514-131">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="21514-132">O servidor está lento para responder.</span><span class="sxs-lookup"><span data-stu-id="21514-132">The server is slow to respond.</span></span>  <span data-ttu-id="21514-133">Hospede o servidor localmente para determinar se ele é a conexão ou o servidor que está lento.</span><span class="sxs-lookup"><span data-stu-id="21514-133">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="21514-134">Se você ainda receber um tempo lento para o primeiro byte \ (TTFB \) ao acessar um servidor local, então o servidor está lento.</span><span class="sxs-lookup"><span data-stu-id="21514-134">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="21514-135">Corrige</span><span class="sxs-lookup"><span data-stu-id="21514-135">Fixes</span></span>**  

*   <span data-ttu-id="21514-136">Se a conexão for lenta, considere hospedar o conteúdo em uma CDN ou alterar provedores de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="21514-136">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="21514-137">Se o servidor estiver lento, considere a otimização de consultas de banco de dados, a implementação de um cache ou a modificação da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="21514-137">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <span data-ttu-id="21514-138">Download de conteúdo lento</span><span class="sxs-lookup"><span data-stu-id="21514-138">Slow content download</span></span>   

**<span data-ttu-id="21514-139">Sintomas</span><span class="sxs-lookup"><span data-stu-id="21514-139">Symptoms</span></span>**  

<span data-ttu-id="21514-140">Uma solicitação demora muito tempo para baixar.</span><span class="sxs-lookup"><span data-stu-id="21514-140">A request takes a long time to download.</span></span>  

<span data-ttu-id="21514-141">Na figura a seguir, a barra azul longa na **cascata** ao lado do png significa que demorou muito tempo para baixar.</span><span class="sxs-lookup"><span data-stu-id="21514-141">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Um exemplo de uma solicitação que demora muito tempo para baixar" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="21514-143">Um exemplo de uma solicitação que demora muito tempo para baixar</span><span class="sxs-lookup"><span data-stu-id="21514-143">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="21514-144">Causas</span><span class="sxs-lookup"><span data-stu-id="21514-144">Causes</span></span>**  

*   <span data-ttu-id="21514-145">A conexão entre o cliente e o servidor está lenta.</span><span class="sxs-lookup"><span data-stu-id="21514-145">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="21514-146">Uma grande quantidade de conteúdo está sendo baixada.</span><span class="sxs-lookup"><span data-stu-id="21514-146">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="21514-147">Corrige</span><span class="sxs-lookup"><span data-stu-id="21514-147">Fixes</span></span>**  

*   <span data-ttu-id="21514-148">Considere hospedar o conteúdo em uma CDN ou alterar provedores de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="21514-148">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="21514-149">Envie menos bytes otimizando suas solicitações.</span><span class="sxs-lookup"><span data-stu-id="21514-149">Send fewer bytes by optimizing your requests.</span></span>  
    
## <span data-ttu-id="21514-150">Conhecimento do Contribute</span><span class="sxs-lookup"><span data-stu-id="21514-150">Contribute knowledge</span></span>  

<span data-ttu-id="21514-151">Você tem um problema de rede que deve ser adicionado a este guia?</span><span class="sxs-lookup"><span data-stu-id="21514-151">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="21514-152">Envie um tweet para [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="21514-152">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="21514-153">Selecione **enviar comentários** \ ( ![ enviar comentários ][ImageSendFeedbackIcon] \) no devtools ou pressione `Alt` + `Shift` + `I` \ (Windows \) ou `Option` + `Shift` + `I` \ (MacOS \) para fornecer comentários ou solicitações de recursos.</span><span class="sxs-lookup"><span data-stu-id="21514-153">Select **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="21514-154">[Abra um problema][WebFundamentalsIssue] no repositório de documentos.</span><span class="sxs-lookup"><span data-stu-id="21514-154">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspecionar atividades de rede no Microsoft Edge DevTools | Documentos da Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Novo problema-MicrosoftDocs/Edge-Developer"  

> [!NOTE]
> <span data-ttu-id="21514-157">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="21514-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="21514-158">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/issues) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Jonathan Garbee][JonathanGarbee] \ (Google Developer expert para tecnologia da Web \).</span><span class="sxs-lookup"><span data-stu-id="21514-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="21514-160">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="21514-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
