---
title: Exibir dados de cache com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612065"
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





# <span data-ttu-id="f951a-103">Exibir dados de cache com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f951a-103">View Cache Data With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="f951a-104">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar dados de [cache][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="f951a-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="f951a-105">Se você estiver tentando inspecionar dados de [cache http][MDNHTTPCaching] , este não é o guia desejado.</span><span class="sxs-lookup"><span data-stu-id="f951a-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  
<span data-ttu-id="f951a-106">Procure as informações na coluna **tamanho** do **log de rede**.</span><span class="sxs-lookup"><span data-stu-id="f951a-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="f951a-107">Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="f951a-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="f951a-108">Exibir dados do cache</span><span class="sxs-lookup"><span data-stu-id="f951a-108">View cache data</span></span>   

1.  <span data-ttu-id="f951a-109">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="f951a-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="f951a-110">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="f951a-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="f951a-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="f951a-111">Figure 1</span></span>  
    > <span data-ttu-id="f951a-112">Painel de manifesto</span><span class="sxs-lookup"><span data-stu-id="f951a-112">The Manifest pane</span></span>  
    > ![Painel de manifesto][ImageManifestPane]  

1.  <span data-ttu-id="f951a-114">Expanda a seção **armazenamento do cache** para ver os caches disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f951a-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    > ##### <span data-ttu-id="f951a-115">Figura 2</span><span class="sxs-lookup"><span data-stu-id="f951a-115">Figure 2</span></span>  
    > <span data-ttu-id="f951a-116">Caches disponíveis</span><span class="sxs-lookup"><span data-stu-id="f951a-116">Available caches</span></span>  
    > ![Caches disponíveis][ImageCache]  

1.  <span data-ttu-id="f951a-118">Selecione um cache para exibir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f951a-118">Select a cache to view the contents.</span></span>  
    
    > ##### <span data-ttu-id="f951a-119">Figura 3</span><span class="sxs-lookup"><span data-stu-id="f951a-119">Figure 3</span></span>  
    > <span data-ttu-id="f951a-120">Exibir o conteúdo de um cache</span><span class="sxs-lookup"><span data-stu-id="f951a-120">Viewing the contents of a cache</span></span>  
    > ![Exibir o conteúdo de um cache][ImageCacheView]  

1.  <span data-ttu-id="f951a-122">Selecione um recurso para exibir os cabeçalhos HTTP na seção abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="f951a-122">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    > ##### <span data-ttu-id="f951a-123">Figura 4</span><span class="sxs-lookup"><span data-stu-id="f951a-123">Figure 4</span></span>  
    > <span data-ttu-id="f951a-124">Visualizando os cabeçalhos HTTP de um recurso</span><span class="sxs-lookup"><span data-stu-id="f951a-124">Viewing the HTTP headers of a resource</span></span>  
    > ![Visualizando os cabeçalhos HTTP de um recurso][ImageViewCacheResource]  

1.  <span data-ttu-id="f951a-126">Selecione **Visualizar** para exibir o conteúdo de um recurso.</span><span class="sxs-lookup"><span data-stu-id="f951a-126">Select **Preview** to view the content of a resource.</span></span>  
    
    > ##### <span data-ttu-id="f951a-127">Figura 5</span><span class="sxs-lookup"><span data-stu-id="f951a-127">Figure 5</span></span>  
    > <span data-ttu-id="f951a-128">Exibindo o conteúdo de um recurso</span><span class="sxs-lookup"><span data-stu-id="f951a-128">Viewing the content of a resource</span></span>  
    > ![Exibindo o conteúdo de um recurso][ImageCacheContent]  

## <span data-ttu-id="f951a-130">Atualizar um recurso</span><span class="sxs-lookup"><span data-stu-id="f951a-130">Refresh a resource</span></span>   

1.  <span data-ttu-id="f951a-131">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="f951a-131">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="f951a-132">Selecione o recurso que você deseja atualizar.</span><span class="sxs-lookup"><span data-stu-id="f951a-132">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="f951a-133">O DevTools a destaca para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="f951a-133">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="f951a-134">Figura 6</span><span class="sxs-lookup"><span data-stu-id="f951a-134">Figure 6</span></span>  
    > <span data-ttu-id="f951a-135">Selecionando um recurso</span><span class="sxs-lookup"><span data-stu-id="f951a-135">Selecting a resource</span></span>  
    > ![Selecionando um recurso][ImageCacheSelected]  

1.  <span data-ttu-id="f951a-137">Selecione **Atualizar** ![ atualização ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="f951a-137">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="f951a-138">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="f951a-138">Filter resources</span></span>   

1.  <span data-ttu-id="f951a-139">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="f951a-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="f951a-140">Use a caixa de texto **Filtrar por caminho** para filtrar os recursos que não correspondem ao caminho fornecido.</span><span class="sxs-lookup"><span data-stu-id="f951a-140">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    > ##### <span data-ttu-id="f951a-141">Figura 7</span><span class="sxs-lookup"><span data-stu-id="f951a-141">Figure 7</span></span>  
    > <span data-ttu-id="f951a-142">Filtrar recursos que não correspondem ao caminho especificado</span><span class="sxs-lookup"><span data-stu-id="f951a-142">Filtering out resources that do not match the specified path</span></span>  
    > ![Filtrar recursos que não correspondem ao caminho especificado][ImageCacheFilter]  

## <span data-ttu-id="f951a-144">Excluir um recurso</span><span class="sxs-lookup"><span data-stu-id="f951a-144">Delete a resource</span></span>   

1.  <span data-ttu-id="f951a-145">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="f951a-145">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="f951a-146">Selecione o recurso que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="f951a-146">Select the resource that you want to delete.</span></span>  <span data-ttu-id="f951a-147">O DevTools a destaca para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="f951a-147">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="f951a-148">Figura 8</span><span class="sxs-lookup"><span data-stu-id="f951a-148">Figure 8</span></span>  
    > <span data-ttu-id="f951a-149">Selecionando um recurso</span><span class="sxs-lookup"><span data-stu-id="f951a-149">Selecting a resource</span></span>  
    > ![Selecionando um recurso][ImageCacheSelected2]  

1.  <span data-ttu-id="f951a-151">Selecione **excluir** selecionado ![ excluir selecionado ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="f951a-151">Select **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="f951a-152">Excluir todos os dados do cache</span><span class="sxs-lookup"><span data-stu-id="f951a-152">Delete all cache data</span></span>   

1.  <span data-ttu-id="f951a-153">Abrir **Application**  >  **armazenamento limpo**do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f951a-153">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="f951a-154">Verifique se a caixa de seleção **armazenamento do cache** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f951a-154">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="f951a-155">Figura 9</span><span class="sxs-lookup"><span data-stu-id="f951a-155">Figure 9</span></span>  
    > <span data-ttu-id="f951a-156">A caixa de seleção **armazenamento do cache**</span><span class="sxs-lookup"><span data-stu-id="f951a-156">The **Cache Storage** checkbox</span></span>  
    > ![A caixa de seleção armazenamento do cache][ImageCacheCheckbox]  

1.  <span data-ttu-id="f951a-158">Selecione **limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="f951a-158">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="f951a-159">Figura 10</span><span class="sxs-lookup"><span data-stu-id="f951a-159">Figure 10</span></span>  
    > <span data-ttu-id="f951a-160">O botão **limpar dados do site**</span><span class="sxs-lookup"><span data-stu-id="f951a-160">The **Clear Site Data** button</span></span>  
    > ![O botão limpar dados do site][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Figura 2: caches disponíveis"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Figura 3: exibindo o conteúdo de um cache"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Figura 4: exibindo os cabeçalhos HTTP de um recurso"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Figura 5: exibindo o conteúdo de um recurso"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Figura 6: selecionando um recurso"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Figura 7: filtrando recursos que não correspondem ao caminho especificado"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Figura 8: selecionando um recurso"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Figura 9: caixa de seleção armazenamento do cache"  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Figura 10: o botão limpar dados do site"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Registrar atividades de rede"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="f951a-176">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="f951a-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f951a-177">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/cache) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f951a-177">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f951a-179">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f951a-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
