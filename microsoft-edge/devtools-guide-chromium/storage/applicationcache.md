---
description: Como exibir dados de cache do aplicativo no painel de aplicativos do Microsoft Edge DevTools.
title: Exibir dados de cache do aplicativo com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ed742f24900786c3c5b31ec2a026ddbf9d16ccb6
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993321"
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

# <span data-ttu-id="7f85e-104">Exibir dados de cache do aplicativo com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7f85e-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="7f85e-105">A API de cache do aplicativo está [sendo removida da plataforma da Web][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="7f85e-105">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="7f85e-106">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar os recursos de [cache do aplicativo][MDNWebAPIsWindowApplicationCache] .</span><span class="sxs-lookup"><span data-stu-id="7f85e-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="7f85e-107">Exibir dados de cache do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7f85e-107">View Application Cache data</span></span>  

1.  <span data-ttu-id="7f85e-108">Selecione a guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="7f85e-108">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="7f85e-109">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="7f85e-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="7f85e-111">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="7f85e-111">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="7f85e-112">Expanda a seção **cache do aplicativo** e escolha um cache para ver os recursos.</span><span class="sxs-lookup"><span data-stu-id="7f85e-112">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Painel de cache do aplicativo" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="7f85e-114">Painel de **cache do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="7f85e-114">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="7f85e-115">Cada linha da tabela representa um recurso armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="7f85e-115">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="7f85e-116">A coluna **tipo** representa a [categoria do recurso][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="7f85e-116">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="7f85e-117">Categoria</span><span class="sxs-lookup"><span data-stu-id="7f85e-117">Category</span></span> | <span data-ttu-id="7f85e-118">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7f85e-118">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="7f85e-119">Este recurso foi explicitamente listado no manifesto.</span><span class="sxs-lookup"><span data-stu-id="7f85e-119">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="7f85e-120">A URL é um fallback para outro recurso.</span><span class="sxs-lookup"><span data-stu-id="7f85e-120">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="7f85e-121">A URL do outro recurso não está listada no DevTools.</span><span class="sxs-lookup"><span data-stu-id="7f85e-121">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="7f85e-122">O `manifest` atributo no recurso indica que o cache é o pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="7f85e-122">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="7f85e-123">O manifesto especificou que o recurso deve vir da rede.</span><span class="sxs-lookup"><span data-stu-id="7f85e-123">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="7f85e-124">Na parte inferior da tabela há ícones de status que indicam a conexão de rede e o status do **cache do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="7f85e-124">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="7f85e-125">O **cache do aplicativo** pode ter os seguintes Estados.</span><span class="sxs-lookup"><span data-stu-id="7f85e-125">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="7f85e-126">Estado</span><span class="sxs-lookup"><span data-stu-id="7f85e-126">State</span></span> | <span data-ttu-id="7f85e-127">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7f85e-127">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="7f85e-128">O manifesto está sendo buscado e verificou se há atualizações.</span><span class="sxs-lookup"><span data-stu-id="7f85e-128">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="7f85e-129">Os recursos estão sendo adicionados ao cache.</span><span class="sxs-lookup"><span data-stu-id="7f85e-129">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="7f85e-130">O cache não tem novas alterações.</span><span class="sxs-lookup"><span data-stu-id="7f85e-130">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="7f85e-131">O cache está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="7f85e-131">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="7f85e-132">Uma nova versão do cache está disponível.</span><span class="sxs-lookup"><span data-stu-id="7f85e-132">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicativos Web offline-padrão HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos em um cache de aplicativos | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-APIs da Web | MDN"  

> [!NOTE]
> <span data-ttu-id="7f85e-137">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="7f85e-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7f85e-138">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7f85e-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7f85e-140">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7f85e-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
