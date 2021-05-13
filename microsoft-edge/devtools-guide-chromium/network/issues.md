---
description: Saiba como detectar problemas de rede no painel Rede do Microsoft Edge DevTools.
title: Guia de problemas de rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c99f43872abe04800880c63ee4126bfcdd633edb
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564977"
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
# <a name="network-issues-guide"></a><span data-ttu-id="96d41-104">Guia de problemas de rede</span><span class="sxs-lookup"><span data-stu-id="96d41-104">Network issues guide</span></span>  

<span data-ttu-id="96d41-105">Este guia mostra como detectar problemas de rede ou oportunidades de otimização no painel Rede do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="96d41-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="96d41-106">Para saber os conceitos básicos da **ferramenta Rede,** navegue até [Introdução][NetworkPerformance].</span><span class="sxs-lookup"><span data-stu-id="96d41-106">To learn the basics of the **Network** tool, navigate to [Get Started][NetworkPerformance].</span></span>  

## <a name="queued-or-stalled-requests"></a><span data-ttu-id="96d41-107">Solicitações em fila ou paralisadas</span><span class="sxs-lookup"><span data-stu-id="96d41-107">Queued or stalled requests</span></span>  

**<span data-ttu-id="96d41-108">Sintomas</span><span class="sxs-lookup"><span data-stu-id="96d41-108">Symptoms</span></span>**  

<span data-ttu-id="96d41-109">Seis solicitações estão sendo baixadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="96d41-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="96d41-110">Depois disso, uma série de solicitações são enluadas ou paralisadas.</span><span class="sxs-lookup"><span data-stu-id="96d41-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="96d41-111">Quando uma das seis primeiras solicitações é final, uma das solicitações na fila é iniciada.</span><span class="sxs-lookup"><span data-stu-id="96d41-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="96d41-112">Na **Cascata,** na figura a seguir, as seis primeiras solicitações para `edge-iconx1024.msft.png` o ativo começam simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="96d41-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="96d41-113">As solicitações subsequentes são paralisadas até que uma das seis terminações originais.</span><span class="sxs-lookup"><span data-stu-id="96d41-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Um exemplo de uma série em fila ou paralisada no painel Rede" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="96d41-115">Um exemplo de uma série em fila ou paralisada na **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="96d41-115">An example of a queued or stalled series in the **Network** tool</span></span>  
:::image-end:::  

**<span data-ttu-id="96d41-116">Causas</span><span class="sxs-lookup"><span data-stu-id="96d41-116">Causes</span></span>**  

<span data-ttu-id="96d41-117">Muitas solicitações estão sendo feitas em um único domínio.</span><span class="sxs-lookup"><span data-stu-id="96d41-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="96d41-118">Em conexões HTTP/1.0 ou HTTP/1.1, Microsoft Edge permite no máximo seis conexões TCP simultâneas por host.</span><span class="sxs-lookup"><span data-stu-id="96d41-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="96d41-119">Correções</span><span class="sxs-lookup"><span data-stu-id="96d41-119">Fixes</span></span>**  

*   <span data-ttu-id="96d41-120">Implemente o fragmento de domínio se você deve usar HTTP/1.0 ou HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="96d41-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="96d41-121">Use HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="96d41-121">Use HTTP/2.</span></span>  <span data-ttu-id="96d41-122">Não use o fragmento de domínio com HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="96d41-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="96d41-123">Remover ou adiar solicitações desnecessárias para que solicitações críticas baixem anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96d41-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <a name="slow-time-to-first-byte-ttfb"></a><span data-ttu-id="96d41-124">Tempo lento para primeiro byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="96d41-124">Slow Time To First Byte (TTFB)</span></span>  

**<span data-ttu-id="96d41-125">Sintomas</span><span class="sxs-lookup"><span data-stu-id="96d41-125">Symptoms</span></span>**  

<span data-ttu-id="96d41-126">Uma solicitação passa muito tempo esperando para receber o primeiro byte do servidor.</span><span class="sxs-lookup"><span data-stu-id="96d41-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="96d41-127">Na figura a seguir, a barra longa e verde na **Cascata** indica que a solicitação estava aguardando muito tempo.</span><span class="sxs-lookup"><span data-stu-id="96d41-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="96d41-128">Isso foi simulado usando um perfil para restringir a velocidade da rede e adicionar um atraso.</span><span class="sxs-lookup"><span data-stu-id="96d41-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Um exemplo de uma solicitação com um tempo lento para o primeiro byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="96d41-130">Um exemplo de uma solicitação com um tempo lento para o primeiro byte</span><span class="sxs-lookup"><span data-stu-id="96d41-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="96d41-131">Causas</span><span class="sxs-lookup"><span data-stu-id="96d41-131">Causes</span></span>**  

*   <span data-ttu-id="96d41-132">A conexão entre o cliente e o servidor é lenta.</span><span class="sxs-lookup"><span data-stu-id="96d41-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="96d41-133">O servidor é lento para responder.</span><span class="sxs-lookup"><span data-stu-id="96d41-133">The server is slow to respond.</span></span>  <span data-ttu-id="96d41-134">Hospede o servidor localmente para determinar se é a conexão ou o servidor que está lento.</span><span class="sxs-lookup"><span data-stu-id="96d41-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="96d41-135">Se você ainda tiver um tempo lento para o primeiro byte \(TTFB\) ao acessar um servidor local, o servidor será lento.</span><span class="sxs-lookup"><span data-stu-id="96d41-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="96d41-136">Correções</span><span class="sxs-lookup"><span data-stu-id="96d41-136">Fixes</span></span>**  

*   <span data-ttu-id="96d41-137">Se a conexão for lenta, considere hospedar seu conteúdo em um CDN ou alterar provedores de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="96d41-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="96d41-138">Se o servidor for lento, considere otimizar consultas de banco de dados, implementar um cache ou modificar a configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="96d41-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <a name="slow-content-download"></a><span data-ttu-id="96d41-139">Download de conteúdo lento</span><span class="sxs-lookup"><span data-stu-id="96d41-139">Slow content download</span></span>  

**<span data-ttu-id="96d41-140">Sintomas</span><span class="sxs-lookup"><span data-stu-id="96d41-140">Symptoms</span></span>**  

<span data-ttu-id="96d41-141">Uma solicitação leva muito tempo para ser baixada.</span><span class="sxs-lookup"><span data-stu-id="96d41-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="96d41-142">Na figura a seguir, a barra longa e azul na **Cascata** ao lado do png significa que demorou muito para ser baixado.</span><span class="sxs-lookup"><span data-stu-id="96d41-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Um exemplo de uma solicitação que leva muito tempo para ser baixada" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="96d41-144">Um exemplo de uma solicitação que leva muito tempo para ser baixada</span><span class="sxs-lookup"><span data-stu-id="96d41-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="96d41-145">Causas</span><span class="sxs-lookup"><span data-stu-id="96d41-145">Causes</span></span>**  

*   <span data-ttu-id="96d41-146">A conexão entre o cliente e o servidor é lenta.</span><span class="sxs-lookup"><span data-stu-id="96d41-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="96d41-147">Muito conteúdo está sendo baixado.</span><span class="sxs-lookup"><span data-stu-id="96d41-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="96d41-148">Correções</span><span class="sxs-lookup"><span data-stu-id="96d41-148">Fixes</span></span>**  

*   <span data-ttu-id="96d41-149">Considere hospedar seu conteúdo em um CDN ou alterar provedores de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="96d41-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="96d41-150">Envie menos bytes otimizando suas solicitações.</span><span class="sxs-lookup"><span data-stu-id="96d41-150">Send fewer bytes by optimizing your requests.</span></span>  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback](../media/smile-icon.msft.png)\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="96d41-151">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="96d41-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

> [!NOTE]
> <span data-ttu-id="96d41-154">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96d41-154">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="96d41-155">A página original [](https://developers.google.com/web/tools/chrome-devtools/network/issues) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span><span class="sxs-lookup"><span data-stu-id="96d41-155">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="96d41-157">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96d41-157">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors#jonathan-garbee
