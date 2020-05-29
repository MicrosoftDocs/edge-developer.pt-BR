---
title: Entender problemas de segurança com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611907"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="071a1-103">Entender problemas de segurança com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="071a1-103">Understand Security Issues With Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="071a1-104">Abrir o painel de segurança</span><span class="sxs-lookup"><span data-stu-id="071a1-104">Open the Security panel</span></span>   

<span data-ttu-id="071a1-105">O painel de **segurança** é o local principal no devtools para inspecionar a segurança de uma página.</span><span class="sxs-lookup"><span data-stu-id="071a1-105">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="071a1-106">[Abra o devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="071a1-106">[Open DevTools][DevToolsOpen].</span></span>  

1.  <span data-ttu-id="071a1-107">Clique na guia **segurança** para abrir o painel **segurança** .</span><span class="sxs-lookup"><span data-stu-id="071a1-107">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    > ##### <span data-ttu-id="071a1-108">Figura 1</span><span class="sxs-lookup"><span data-stu-id="071a1-108">Figure 1</span></span>  
    > <span data-ttu-id="071a1-109">O painel de segurança</span><span class="sxs-lookup"><span data-stu-id="071a1-109">The Security panel</span></span>  
    > ![O painel de segurança][ImageSecurityPanel]  
    
## <span data-ttu-id="071a1-111">Problemas comuns</span><span class="sxs-lookup"><span data-stu-id="071a1-111">Common problems</span></span>   

### <span data-ttu-id="071a1-112">Origens principais não seguras</span><span class="sxs-lookup"><span data-stu-id="071a1-112">Non-secure main origins</span></span>   

<span data-ttu-id="071a1-113">Quando a origem principal de uma página não é segura, a **visão geral da segurança** diz que **esta página não é segura**.</span><span class="sxs-lookup"><span data-stu-id="071a1-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

> ##### <span data-ttu-id="071a1-114">Figura 2</span><span class="sxs-lookup"><span data-stu-id="071a1-114">Figure 2</span></span>  
> <span data-ttu-id="071a1-115">Uma página não segura</span><span class="sxs-lookup"><span data-stu-id="071a1-115">A non-secure page</span></span>  
> ![Uma página não segura][ImageNonSecurePage]  

<span data-ttu-id="071a1-117">Esse problema ocorre quando a URL que você visitou era solicitada por HTTP.</span><span class="sxs-lookup"><span data-stu-id="071a1-117">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="071a1-118">Para torná-lo seguro, você precisa solicitá-lo por HTTPS.</span><span class="sxs-lookup"><span data-stu-id="071a1-118">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="071a1-119">Por exemplo, se você olhar para a URL na barra de endereços, provavelmente ela terá uma aparência semelhante `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="071a1-119">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="071a1-120">Para torná-lo seguro, a URL deve estar `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="071a1-120">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="071a1-121">Se você já configurou o HTTPS em seu servidor, tudo o que precisa fazer para corrigir esse problema é configurar seu servidor para redirecionar todas as solicitações HTTP para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="071a1-121">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="071a1-122">Se você não configurou HTTPS em seu servidor, [vamos criptografar][LetsEncrypt] uma maneira gratuita e fácil de iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="071a1-122">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="071a1-123">Ou você pode considerar hospedar seu site em uma CDN.</span><span class="sxs-lookup"><span data-stu-id="071a1-123">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="071a1-124">A maioria dos principais sites de host do CDNs em HTTPS, por padrão, agora.</span><span class="sxs-lookup"><span data-stu-id="071a1-124">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="071a1-125">A dica [use HTTPS][WebhintUseHttps] na [webhint][Webhint] pode ajudar a automatizar o processo de verificar se todas as solicitações HTTP são direcionadas para https.</span><span class="sxs-lookup"><span data-stu-id="071a1-125">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="071a1-126">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="071a1-126">Mixed content</span></span>   

<span data-ttu-id="071a1-127">**Conteúdo misto** significa que a origem principal de uma página é segura, mas a página solicitou recursos de origens não seguras.</span><span class="sxs-lookup"><span data-stu-id="071a1-127">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="071a1-128">Páginas de conteúdo misto são apenas parcialmente protegidas porque o conteúdo HTTP está acessível a farejadores e vulneráveis a ataques de Man-in-the-Middle.</span><span class="sxs-lookup"><span data-stu-id="071a1-128">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

> ##### <span data-ttu-id="071a1-129">Figura 3</span><span class="sxs-lookup"><span data-stu-id="071a1-129">Figure 3</span></span>  
> <span data-ttu-id="071a1-130">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="071a1-130">Mixed content</span></span>  
> ![Conteúdo misto][ImageMixedContent]  

<span data-ttu-id="071a1-132">Na [Figura 3](#figure-3), clique em **Exibir 1 solicitação no painel de rede** para abrir o painel de **rede** e aplicar o `mixed-content:displayed` filtro para que o **log de rede** mostre apenas os recursos não seguros.</span><span class="sxs-lookup"><span data-stu-id="071a1-132">In [Figure 3](#figure-3), click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

> ##### <span data-ttu-id="071a1-133">Figura 4</span><span class="sxs-lookup"><span data-stu-id="071a1-133">Figure 4</span></span>  
> <span data-ttu-id="071a1-134">Recursos mistos no log de rede</span><span class="sxs-lookup"><span data-stu-id="071a1-134">Mixed resources in the Network Log</span></span>  
> ![Recursos mistos no log de rede][ImageMixedResourcesNetworkLog]  

## <span data-ttu-id="071a1-136">Exibir detalhes</span><span class="sxs-lookup"><span data-stu-id="071a1-136">View details</span></span>   

### <span data-ttu-id="071a1-137">Exibir certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="071a1-137">View main origin certificate</span></span>   

<span data-ttu-id="071a1-138">Na **visão geral de segurança**, clique em **Exibir certificado** para inspecionar rapidamente o certificado para a origem principal.</span><span class="sxs-lookup"><span data-stu-id="071a1-138">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

> ##### <span data-ttu-id="071a1-139">Figura 5</span><span class="sxs-lookup"><span data-stu-id="071a1-139">Figure 5</span></span>  
> <span data-ttu-id="071a1-140">Um certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="071a1-140">A main origin certificate</span></span>  
> ![Um certificado de origem principal][ImageCertificate]  

### <span data-ttu-id="071a1-142">Exibir detalhes da origem</span><span class="sxs-lookup"><span data-stu-id="071a1-142">View origin details</span></span>   

<span data-ttu-id="071a1-143">Clique em uma das entradas na barra de navegação à esquerda para exibir os detalhes da origem.</span><span class="sxs-lookup"><span data-stu-id="071a1-143">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="071a1-144">Na página detalhes, você pode exibir informações de conexão e certificado.</span><span class="sxs-lookup"><span data-stu-id="071a1-144">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="071a1-145">As informações sobre transparência do certificado também são mostradas quando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="071a1-145">Certificate transparency information is also shown when available.</span></span>  

> ##### <span data-ttu-id="071a1-146">Figura 6</span><span class="sxs-lookup"><span data-stu-id="071a1-146">Figure 6</span></span>  
> <span data-ttu-id="071a1-147">Detalhes da origem principal</span><span class="sxs-lookup"><span data-stu-id="071a1-147">Main origin details</span></span>  
> ![Detalhes da origem principal][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Figura 1: o painel de segurança"  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Figura 2: uma página não segura"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Figura 3: conteúdo misto"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Figura 4: recursos mistos no log de rede"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Figura 5: certificado de origem principal"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Figura 6: detalhes da origem principal"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools"  


[LetsEncrypt]: https://letsencrypt.org "Vamos criptografar certificados SSL/TLS grátis"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar HTTPS | documentação do webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="071a1-160">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="071a1-160">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="071a1-161">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/security/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="071a1-161">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="071a1-163">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="071a1-163">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
