---
description: Use o Painel de Segurança para garantir que uma página seja totalmente protegida por HTTPS.
title: Compreender problemas de segurança com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397773"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a><span data-ttu-id="fbd4a-104">Compreender problemas de segurança com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fbd4a-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a><span data-ttu-id="fbd4a-105">Abra o painel Segurança</span><span class="sxs-lookup"><span data-stu-id="fbd4a-105">Open the Security panel</span></span>  

<span data-ttu-id="fbd4a-106">O **painel** Segurança é o principal local no DevTools para inspecionar a segurança de uma página.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="fbd4a-107">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="fbd4a-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="fbd4a-108">Escolha a **guia Segurança** para abrir a **ferramenta Segurança.**</span><span class="sxs-lookup"><span data-stu-id="fbd4a-108">Choose the **Security** tab to open the **Security** tool.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="O painel Segurança" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="fbd4a-110">O **painel Segurança**</span><span class="sxs-lookup"><span data-stu-id="fbd4a-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <a name="common-problems"></a><span data-ttu-id="fbd4a-111">Problemas comuns</span><span class="sxs-lookup"><span data-stu-id="fbd4a-111">Common problems</span></span>  

### <a name="non-secure-main-origins"></a><span data-ttu-id="fbd4a-112">Origens principais não seguras</span><span class="sxs-lookup"><span data-stu-id="fbd4a-112">Non-secure main origins</span></span>  

<span data-ttu-id="fbd4a-113">Quando a origem principal de uma página não é segura, a Visão Geral de Segurança **diz** que esta página não **é segura**.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Uma página não segura" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="fbd4a-115">Uma página não segura</span><span class="sxs-lookup"><span data-stu-id="fbd4a-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="fbd4a-116">Esse problema ocorre quando a URL que você visitou foi solicitada por HTTP.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="fbd4a-117">Para torná-lo seguro, você precisa solicitá-lo por HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="fbd4a-118">Por exemplo, se você olhar para a URL na barra de endereços, provavelmente será semelhante a `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="fbd4a-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="fbd4a-119">Para torná-la segura, a URL deve ser `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="fbd4a-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="fbd4a-120">Se você já configurou HTTPS em seu servidor, tudo o que você precisa fazer para corrigir esse problema é configurar seu servidor para redirecionar todas as solicitações HTTP para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="fbd4a-121">Se você não tiver definido HTTPS em seu servidor, [Vamos][LetsEncrypt] Criptografar fornece uma maneira gratuita e relativamente fácil de iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="fbd4a-122">Ou você pode considerar hospedar seu site em uma CDN.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-122">Or, you may consider hosting your site on a CDN.</span></span>  <span data-ttu-id="fbd4a-123">A maioria dos principais sites de host de CDNs em HTTPS por padrão agora.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="fbd4a-124">A [dica Usar HTTPS][WebhintUseHttps] na [webhint][Webhint] pode ajudar a automatizar o processo de garantir que todas as solicitações HTTP sejam direcionadas para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <a name="mixed-content"></a><span data-ttu-id="fbd4a-125">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="fbd4a-125">Mixed content</span></span>  

<span data-ttu-id="fbd4a-126">**O conteúdo** misto significa que a origem principal de uma página é segura, mas a página solicitou recursos de origens não seguras.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="fbd4a-127">Páginas de conteúdo misto só são parcialmente protegidas porque o conteúdo HTTP é acessível a farejadores e vulnerável a ataques de homem no meio.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Conteúdo misto" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="fbd4a-129">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="fbd4a-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="fbd4a-130">Na figura anterior, escolha **Exibir uma** solicitação  no painel Rede para abrir a ferramenta Rede e aplicar o filtro para que o Log de Rede mostre apenas recursos `mixed-content:displayed` não seguros. </span><span class="sxs-lookup"><span data-stu-id="fbd4a-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** tool and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Recursos mistos no Log de Rede" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="fbd4a-132">Recursos mistos no **Log de Rede**</span><span class="sxs-lookup"><span data-stu-id="fbd4a-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <a name="view-details"></a><span data-ttu-id="fbd4a-133">Exibir detalhes</span><span class="sxs-lookup"><span data-stu-id="fbd4a-133">View details</span></span>  

### <a name="view-main-origin-certificate"></a><span data-ttu-id="fbd4a-134">Exibir certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="fbd4a-134">View main origin certificate</span></span>  

<span data-ttu-id="fbd4a-135">Na Visão **Geral de**Segurança, escolha **Exibir certificado** para inspecionar rapidamente o certificado para a origem principal.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Um certificado de origem principal" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="fbd4a-137">Um certificado de origem principal</span><span class="sxs-lookup"><span data-stu-id="fbd4a-137">A main origin certificate</span></span>  
:::image-end:::  

### <a name="view-origin-details"></a><span data-ttu-id="fbd4a-138">Exibir detalhes de origem</span><span class="sxs-lookup"><span data-stu-id="fbd4a-138">View origin details</span></span>  

<span data-ttu-id="fbd4a-139">Escolha uma das entradas na nav à esquerda para exibir os detalhes da origem.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-139">Choose one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="fbd4a-140">Na página de detalhes, você pode exibir informações de conexão e certificado.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="fbd4a-141">As informações de transparência do certificado também são mostradas quando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fbd4a-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Detalhes de origem principal" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="fbd4a-143">Detalhes de origem principal</span><span class="sxs-lookup"><span data-stu-id="fbd4a-143">Main origin details</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="fbd4a-144">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fbd4a-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevToolsOpen]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  

[LetsEncrypt]: https://letsencrypt.org "Vamos criptografar - certificados SSL/TLS gratuitos"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Use HTTPS | documentação webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="fbd4a-150">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fbd4a-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fbd4a-151">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/security/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="fbd4a-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fbd4a-153">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fbd4a-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
