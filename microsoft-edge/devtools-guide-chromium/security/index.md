---
title: Entender problemas de segurança com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 850dde157a673a84a3e603f22a5e54abd90bde5d
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984286"
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





# <span data-ttu-id="47239-103">Entender problemas de segurança com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="47239-103">Understand security issues with Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="47239-104">Abrir o painel de segurança</span><span class="sxs-lookup"><span data-stu-id="47239-104">Open the Security panel</span></span>   

<span data-ttu-id="47239-105">O painel de **segurança** é o local principal no devtools para inspecionar a segurança de uma página.</span><span class="sxs-lookup"><span data-stu-id="47239-105">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="47239-106">[Abra o devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="47239-106">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="47239-107">Clique na guia **segurança** para abrir o painel **segurança** .</span><span class="sxs-lookup"><span data-stu-id="47239-107">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="O painel de segurança" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="47239-109">O painel de **segurança**</span><span class="sxs-lookup"><span data-stu-id="47239-109">The **Security** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="47239-110">Problemas comuns</span><span class="sxs-lookup"><span data-stu-id="47239-110">Common problems</span></span>   

### <span data-ttu-id="47239-111">Origens principais não seguras</span><span class="sxs-lookup"><span data-stu-id="47239-111">Non-secure main origins</span></span>   

<span data-ttu-id="47239-112">Quando a origem principal de uma página não é segura, a **visão geral da segurança** diz que **esta página não é segura**.</span><span class="sxs-lookup"><span data-stu-id="47239-112">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Uma página não segura" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="47239-114">Uma página não segura</span><span class="sxs-lookup"><span data-stu-id="47239-114">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="47239-115">Esse problema ocorre quando a URL que você visitou era solicitada por HTTP.</span><span class="sxs-lookup"><span data-stu-id="47239-115">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="47239-116">Para torná-lo seguro, você precisa solicitá-lo por HTTPS.</span><span class="sxs-lookup"><span data-stu-id="47239-116">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="47239-117">Por exemplo, se você olhar para a URL na barra de endereços, provavelmente ela terá uma aparência semelhante `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="47239-117">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="47239-118">Para torná-lo seguro, a URL deve estar `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="47239-118">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="47239-119">Se você já configurou o HTTPS em seu servidor, tudo o que precisa fazer para corrigir esse problema é configurar seu servidor para redirecionar todas as solicitações HTTP para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="47239-119">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="47239-120">Se você não configurou HTTPS em seu servidor, [vamos criptografar][LetsEncrypt] uma maneira gratuita e fácil de iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="47239-120">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="47239-121">Ou você pode considerar hospedar seu site em uma CDN.</span><span class="sxs-lookup"><span data-stu-id="47239-121">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="47239-122">A maioria dos principais sites de host do CDNs em HTTPS, por padrão, agora.</span><span class="sxs-lookup"><span data-stu-id="47239-122">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="47239-123">A dica [use HTTPS][WebhintUseHttps] na [webhint][Webhint] pode ajudar a automatizar o processo de verificar se todas as solicitações HTTP são direcionadas para https.</span><span class="sxs-lookup"><span data-stu-id="47239-123">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="47239-124">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="47239-124">Mixed content</span></span>   

<span data-ttu-id="47239-125">**Conteúdo misto** significa que a origem principal de uma página é segura, mas a página solicitou recursos de origens não seguras.</span><span class="sxs-lookup"><span data-stu-id="47239-125">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="47239-126">Páginas de conteúdo misto são apenas parcialmente protegidas porque o conteúdo HTTP está acessível a farejadores e vulneráveis a ataques de Man-in-the-Middle.</span><span class="sxs-lookup"><span data-stu-id="47239-126">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Conteúdo misto" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="47239-128">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="47239-128">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="47239-129">Na figura anterior, clique em **Exibir 1 solicitação no painel de rede** para abrir o painel de **rede** e aplicar o `mixed-content:displayed` filtro para que o **log de rede** mostre apenas os recursos não seguros.</span><span class="sxs-lookup"><span data-stu-id="47239-129">In the previous figure, click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Recursos mistos no log de rede" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="47239-131">Recursos mistos no **log de rede**</span><span class="sxs-lookup"><span data-stu-id="47239-131">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <span data-ttu-id="47239-132">Exibir detalhes</span><span class="sxs-lookup"><span data-stu-id="47239-132">View details</span></span>   

### <span data-ttu-id="47239-133">Exibir certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="47239-133">View main origin certificate</span></span>   

<span data-ttu-id="47239-134">Na **visão geral de segurança**, clique em **Exibir certificado** para inspecionar rapidamente o certificado para a origem principal.</span><span class="sxs-lookup"><span data-stu-id="47239-134">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Um certificado de origem principal" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="47239-136">Um certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="47239-136">A main origin certificate</span></span>  
:::image-end:::  

### <span data-ttu-id="47239-137">Exibir detalhes da origem</span><span class="sxs-lookup"><span data-stu-id="47239-137">View origin details</span></span>   

<span data-ttu-id="47239-138">Clique em uma das entradas na barra de navegação à esquerda para exibir os detalhes da origem.</span><span class="sxs-lookup"><span data-stu-id="47239-138">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="47239-139">Na página detalhes, você pode exibir informações de conexão e certificado.</span><span class="sxs-lookup"><span data-stu-id="47239-139">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="47239-140">As informações sobre transparência do certificado também são mostradas quando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="47239-140">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Detalhes da origem principal" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="47239-142">Detalhes da origem principal</span><span class="sxs-lookup"><span data-stu-id="47239-142">Main origin details</span></span>  
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
> <span data-ttu-id="47239-148">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="47239-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="47239-149">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/security/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="47239-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="47239-151">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="47239-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
