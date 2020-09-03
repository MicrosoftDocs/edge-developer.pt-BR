---
description: Use o painel de segurança para garantir que uma página seja totalmente protegida por HTTPS.
title: Entender problemas de segurança com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2538f80b08c8162d27f075775075a8b81c5f7725
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993573"
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





# <span data-ttu-id="c29a2-104">Entender problemas de segurança com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c29a2-104">Understand security issues with Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="c29a2-105">Abrir o painel de segurança</span><span class="sxs-lookup"><span data-stu-id="c29a2-105">Open the Security panel</span></span>   

<span data-ttu-id="c29a2-106">O painel de **segurança** é o local principal no devtools para inspecionar a segurança de uma página.</span><span class="sxs-lookup"><span data-stu-id="c29a2-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="c29a2-107">[Abra o devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="c29a2-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="c29a2-108">Clique na guia **segurança** para abrir o painel **segurança** .</span><span class="sxs-lookup"><span data-stu-id="c29a2-108">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="O painel de segurança" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="c29a2-110">O painel de **segurança**</span><span class="sxs-lookup"><span data-stu-id="c29a2-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c29a2-111">Problemas comuns</span><span class="sxs-lookup"><span data-stu-id="c29a2-111">Common problems</span></span>   

### <span data-ttu-id="c29a2-112">Origens principais não seguras</span><span class="sxs-lookup"><span data-stu-id="c29a2-112">Non-secure main origins</span></span>   

<span data-ttu-id="c29a2-113">Quando a origem principal de uma página não é segura, a **visão geral da segurança** diz que **esta página não é segura**.</span><span class="sxs-lookup"><span data-stu-id="c29a2-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Uma página não segura" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="c29a2-115">Uma página não segura</span><span class="sxs-lookup"><span data-stu-id="c29a2-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="c29a2-116">Esse problema ocorre quando a URL que você visitou era solicitada por HTTP.</span><span class="sxs-lookup"><span data-stu-id="c29a2-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="c29a2-117">Para torná-lo seguro, você precisa solicitá-lo por HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c29a2-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="c29a2-118">Por exemplo, se você olhar para a URL na barra de endereços, provavelmente ela terá uma aparência semelhante `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="c29a2-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="c29a2-119">Para torná-lo seguro, a URL deve estar `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="c29a2-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="c29a2-120">Se você já configurou o HTTPS em seu servidor, tudo o que precisa fazer para corrigir esse problema é configurar seu servidor para redirecionar todas as solicitações HTTP para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c29a2-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="c29a2-121">Se você não configurou HTTPS em seu servidor, [vamos criptografar][LetsEncrypt] uma maneira gratuita e fácil de iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="c29a2-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="c29a2-122">Ou você pode considerar hospedar seu site em uma CDN.</span><span class="sxs-lookup"><span data-stu-id="c29a2-122">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="c29a2-123">A maioria dos principais sites de host do CDNs em HTTPS, por padrão, agora.</span><span class="sxs-lookup"><span data-stu-id="c29a2-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="c29a2-124">A dica [use HTTPS][WebhintUseHttps] na [webhint][Webhint] pode ajudar a automatizar o processo de verificar se todas as solicitações HTTP são direcionadas para https.</span><span class="sxs-lookup"><span data-stu-id="c29a2-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="c29a2-125">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="c29a2-125">Mixed content</span></span>   

<span data-ttu-id="c29a2-126">**Conteúdo misto** significa que a origem principal de uma página é segura, mas a página solicitou recursos de origens não seguras.</span><span class="sxs-lookup"><span data-stu-id="c29a2-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="c29a2-127">Páginas de conteúdo misto são apenas parcialmente protegidas porque o conteúdo HTTP está acessível a farejadores e vulneráveis a ataques de Man-in-the-Middle.</span><span class="sxs-lookup"><span data-stu-id="c29a2-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Conteúdo misto" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="c29a2-129">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="c29a2-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="c29a2-130">Na figura anterior, clique em **Exibir 1 solicitação no painel de rede** para abrir o painel de **rede** e aplicar o `mixed-content:displayed` filtro para que o **log de rede** mostre apenas os recursos não seguros.</span><span class="sxs-lookup"><span data-stu-id="c29a2-130">In the previous figure, click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Recursos mistos no log de rede" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="c29a2-132">Recursos mistos no **log de rede**</span><span class="sxs-lookup"><span data-stu-id="c29a2-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <span data-ttu-id="c29a2-133">Exibir detalhes</span><span class="sxs-lookup"><span data-stu-id="c29a2-133">View details</span></span>   

### <span data-ttu-id="c29a2-134">Exibir certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="c29a2-134">View main origin certificate</span></span>   

<span data-ttu-id="c29a2-135">Na **visão geral de segurança**, clique em **Exibir certificado** para inspecionar rapidamente o certificado para a origem principal.</span><span class="sxs-lookup"><span data-stu-id="c29a2-135">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Um certificado de origem principal" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="c29a2-137">Um certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="c29a2-137">A main origin certificate</span></span>  
:::image-end:::  

### <span data-ttu-id="c29a2-138">Exibir detalhes da origem</span><span class="sxs-lookup"><span data-stu-id="c29a2-138">View origin details</span></span>   

<span data-ttu-id="c29a2-139">Clique em uma das entradas na barra de navegação à esquerda para exibir os detalhes da origem.</span><span class="sxs-lookup"><span data-stu-id="c29a2-139">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="c29a2-140">Na página detalhes, você pode exibir informações de conexão e certificado.</span><span class="sxs-lookup"><span data-stu-id="c29a2-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="c29a2-141">As informações sobre transparência do certificado também são mostradas quando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c29a2-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Detalhes da origem principal" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="c29a2-143">Detalhes da origem principal</span><span class="sxs-lookup"><span data-stu-id="c29a2-143">Main origin details</span></span>  
:::image-end:::  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  


[LetsEncrypt]: https://letsencrypt.org "Vamos criptografar certificados SSL/TLS grátis"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar HTTPS | documentação do webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="c29a2-149">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="c29a2-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c29a2-150">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/security/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c29a2-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c29a2-152">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c29a2-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
