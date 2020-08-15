---
title: Exibir dados de cache do aplicativo com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: fc1800fc54e5fb0d7998c62ce163ece7a461dd82
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931202"
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

# <span data-ttu-id="341d9-103">Exibir dados de cache do aplicativo com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="341d9-103">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="341d9-104">A API de cache do aplicativo está [sendo removida da plataforma da Web][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="341d9-104">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="341d9-105">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar os recursos de [cache do aplicativo][MDNWebAPIsWindowApplicationCache] .</span><span class="sxs-lookup"><span data-stu-id="341d9-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="341d9-106">Exibir dados de cache do aplicativo</span><span class="sxs-lookup"><span data-stu-id="341d9-106">View Application Cache data</span></span>  

1.  <span data-ttu-id="341d9-107">Selecione a guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="341d9-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="341d9-108">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="341d9-108">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="341d9-110">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="341d9-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="341d9-111">Expanda a seção **cache do aplicativo** e escolha um cache para ver os recursos.</span><span class="sxs-lookup"><span data-stu-id="341d9-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Painel de cache do aplicativo" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="341d9-113">Painel de **cache do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="341d9-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="341d9-114">Cada linha da tabela representa um recurso armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="341d9-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="341d9-115">A coluna **tipo** representa a [categoria do recurso][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="341d9-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="341d9-116">Categoria</span><span class="sxs-lookup"><span data-stu-id="341d9-116">Category</span></span> | <span data-ttu-id="341d9-117">Detalhes</span><span class="sxs-lookup"><span data-stu-id="341d9-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="341d9-118">Este recurso foi explicitamente listado no manifesto.</span><span class="sxs-lookup"><span data-stu-id="341d9-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="341d9-119">A URL é um fallback para outro recurso.</span><span class="sxs-lookup"><span data-stu-id="341d9-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="341d9-120">A URL do outro recurso não está listada no DevTools.</span><span class="sxs-lookup"><span data-stu-id="341d9-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="341d9-121">O `manifest` atributo no recurso indica que o cache é o pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="341d9-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="341d9-122">O manifesto especificou que o recurso deve vir da rede.</span><span class="sxs-lookup"><span data-stu-id="341d9-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="341d9-123">Na parte inferior da tabela há ícones de status que indicam a conexão de rede e o status do **cache do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="341d9-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="341d9-124">O **cache do aplicativo** pode ter os seguintes Estados.</span><span class="sxs-lookup"><span data-stu-id="341d9-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="341d9-125">Estado</span><span class="sxs-lookup"><span data-stu-id="341d9-125">State</span></span> | <span data-ttu-id="341d9-126">Detalhes</span><span class="sxs-lookup"><span data-stu-id="341d9-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="341d9-127">O manifesto está sendo buscado e verificou se há atualizações.</span><span class="sxs-lookup"><span data-stu-id="341d9-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="341d9-128">Os recursos estão sendo adicionados ao cache.</span><span class="sxs-lookup"><span data-stu-id="341d9-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="341d9-129">O cache não tem novas alterações.</span><span class="sxs-lookup"><span data-stu-id="341d9-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="341d9-130">O cache está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="341d9-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="341d9-131">Uma nova versão do cache está disponível.</span><span class="sxs-lookup"><span data-stu-id="341d9-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicativos Web offline-padrão HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos em um cache de aplicativos | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-APIs da Web | MDN"  

> [!NOTE]
> <span data-ttu-id="341d9-136">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="341d9-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="341d9-137">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="341d9-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="341d9-139">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="341d9-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
