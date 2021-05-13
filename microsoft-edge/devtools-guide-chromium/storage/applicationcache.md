---
description: Como exibir dados de Cache de Aplicativo no painel Aplicativo do Microsoft Edge DevTools.
title: Exibir dados de cache do aplicativo com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ec0d1a003e621ecc2220c3eb0d03992bcd8fffa1
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565019"
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
# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="2a6f6-104">Exibir dados de cache de aplicativo com Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2a6f6-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="2a6f6-105">A API de Cache de Aplicativo [está sendo removida da plataforma Web][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="2a6f6-105">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<!--todo: Replace [HTMLStandardOfflineWebApplications] with [WebDevAppcacheRemoval].  -->  

<span data-ttu-id="2a6f6-106">Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspecionar recursos [de Cache de][MDNWebAPIsWindowApplicationCache] Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <a name="view-application-cache-data"></a><span data-ttu-id="2a6f6-107">Exibir dados do Cache do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2a6f6-107">View Application Cache data</span></span>  

1.  <span data-ttu-id="2a6f6-108">Na parte superior do DevTools, escolha a **ferramenta Application.**</span><span class="sxs-lookup"><span data-stu-id="2a6f6-108">At the top of DevTools, choose the **Application** tool.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="2a6f6-110">O **painel** Manifesto</span><span class="sxs-lookup"><span data-stu-id="2a6f6-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="2a6f6-111">Expanda a **seção Cache** do Aplicativo e escolha um cache para exibir os recursos.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="O painel Cache de Aplicativos" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="2a6f6-113">O **painel Cache** de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2a6f6-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="2a6f6-114">Cada linha da tabela representa um recurso em cache.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="2a6f6-115">A **coluna Tipo** representa a categoria do [recurso][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="2a6f6-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="2a6f6-116">Categoria</span><span class="sxs-lookup"><span data-stu-id="2a6f6-116">Category</span></span> | <span data-ttu-id="2a6f6-117">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2a6f6-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="2a6f6-118">Esse recurso foi explicitamente listado no manifesto.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="2a6f6-119">A URL é um fallback para outro recurso.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="2a6f6-120">A URL do outro recurso não está listada no DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="2a6f6-121">O `manifest` atributo no recurso indica que o cache é o pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="2a6f6-122">O manifesto especificou que o recurso deve vir da rede.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="2a6f6-123">Na parte inferior da tabela, há ícones de status indicando sua conexão de rede e o status do **Cache do Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="2a6f6-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="2a6f6-124">O **Cache de Aplicativo** pode ter os seguintes estados.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="2a6f6-125">Estado</span><span class="sxs-lookup"><span data-stu-id="2a6f6-125">State</span></span> | <span data-ttu-id="2a6f6-126">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2a6f6-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="2a6f6-127">O manifesto está sendo buscado e verificado se há atualizações.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="2a6f6-128">Recursos estão sendo adicionados ao cache.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="2a6f6-129">O cache não tem novas alterações.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="2a6f6-130">O cache está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="2a6f6-131">Uma nova versão do cache está disponível.</span><span class="sxs-lookup"><span data-stu-id="2a6f6-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicativos Web offline - Html Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos em um cache de aplicativo | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache - APIs da Web | MDN"  

[WebDevAppcacheRemoval]: https://web.dev/appcache-removal "Preparando-se para a remoção do AppCache | web.dev"  

> [!NOTE]
> <span data-ttu-id="2a6f6-137">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2a6f6-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2a6f6-138">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2a6f6-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2a6f6-140">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2a6f6-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
