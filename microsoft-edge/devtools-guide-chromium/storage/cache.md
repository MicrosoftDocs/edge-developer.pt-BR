---
title: Exibir dados de cache com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7e7b4326204ce10732972c89b70c966e4bb665fb
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983820"
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





# <span data-ttu-id="b465d-103">Exibir dados de cache com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b465d-103">View cache data with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="b465d-104">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar dados de [cache][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="b465d-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="b465d-105">Se você estiver tentando inspecionar dados de [cache http][MDNHTTPCaching] , este não é o guia desejado.</span><span class="sxs-lookup"><span data-stu-id="b465d-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="b465d-106">Procure as informações na coluna **tamanho** do **log de rede**.</span><span class="sxs-lookup"><span data-stu-id="b465d-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="b465d-107">Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="b465d-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="b465d-108">Exibir dados do cache</span><span class="sxs-lookup"><span data-stu-id="b465d-108">View cache data</span></span>   

1.  <span data-ttu-id="b465d-109">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="b465d-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="b465d-110">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="b465d-110">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="b465d-112">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="b465d-112">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b465d-113">Expanda a seção **armazenamento do cache** para ver os caches disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b465d-113">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Caches disponíveis" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="b465d-115">Caches disponíveis</span><span class="sxs-lookup"><span data-stu-id="b465d-115">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b465d-116">Selecione um cache para exibir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b465d-116">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Exibir o conteúdo de um cache" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="b465d-118">Exibir o conteúdo de um cache</span><span class="sxs-lookup"><span data-stu-id="b465d-118">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b465d-119">Selecione um recurso para exibir os cabeçalhos HTTP na seção abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="b465d-119">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Exibir os cabeçalhos HTTP de um recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="b465d-121">Exibir os cabeçalhos HTTP de um recurso</span><span class="sxs-lookup"><span data-stu-id="b465d-121">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b465d-122">Selecione **Visualizar** para exibir o conteúdo de um recurso.</span><span class="sxs-lookup"><span data-stu-id="b465d-122">Select **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Exibir o conteúdo de um recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="b465d-124">Exibir o conteúdo de um recurso</span><span class="sxs-lookup"><span data-stu-id="b465d-124">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b465d-125">Atualizar um recurso</span><span class="sxs-lookup"><span data-stu-id="b465d-125">Refresh a resource</span></span>   

1.  <span data-ttu-id="b465d-126">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="b465d-126">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="b465d-127">Selecione o recurso que você deseja atualizar.</span><span class="sxs-lookup"><span data-stu-id="b465d-127">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="b465d-128">O DevTools a destaca para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="b465d-128">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Selecionar um recurso" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="b465d-130">Selecionar um recurso</span><span class="sxs-lookup"><span data-stu-id="b465d-130">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b465d-131">Selecione **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b465d-131">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="b465d-132">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="b465d-132">Filter resources</span></span>   

1.  <span data-ttu-id="b465d-133">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="b465d-133">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="b465d-134">Use a caixa de texto **Filtrar por caminho** para filtrar os recursos que não correspondem ao caminho fornecido.</span><span class="sxs-lookup"><span data-stu-id="b465d-134">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que não correspondam ao caminho especificado" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="b465d-136">Filtrar recursos que não correspondam ao caminho especificado</span><span class="sxs-lookup"><span data-stu-id="b465d-136">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b465d-137">Excluir um recurso</span><span class="sxs-lookup"><span data-stu-id="b465d-137">Delete a resource</span></span>   

1.  <span data-ttu-id="b465d-138">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="b465d-138">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="b465d-139">Selecione o recurso que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="b465d-139">Select the resource that you want to delete.</span></span>  <span data-ttu-id="b465d-140">O DevTools a destaca para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="b465d-140">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Selecionar um recurso" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="b465d-142">Selecionar um recurso</span><span class="sxs-lookup"><span data-stu-id="b465d-142">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b465d-143">Selecione **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b465d-143">Select **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="b465d-144">Excluir todos os dados do cache</span><span class="sxs-lookup"><span data-stu-id="b465d-144">Delete all cache data</span></span>   

1.  <span data-ttu-id="b465d-145">Abrir **Application**  >  **armazenamento limpo**do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b465d-145">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="b465d-146">Verifique se a caixa de seleção **armazenamento do cache** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b465d-146">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="A caixa de seleção armazenamento do cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="b465d-148">A caixa de seleção **armazenamento do cache**</span><span class="sxs-lookup"><span data-stu-id="b465d-148">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b465d-149">Selecione **limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="b465d-149">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="O botão limpar dados do site" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="b465d-151">O botão **limpar dados do site**</span><span class="sxs-lookup"><span data-stu-id="b465d-151">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
  


-->  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Registrar atividades da rede | Documentos da Microsoft"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="b465d-156">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="b465d-156">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b465d-157">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/cache) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b465d-157">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b465d-159">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b465d-159">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
