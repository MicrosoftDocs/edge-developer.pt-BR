---
description: Como exibir dados de cache do painel Aplicativo do Microsoft Edge DevTools.
title: Exibir dados de cache com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1f66419014682a316fa565c5ef2ab704f652637f
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564683"
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
# <a name="view-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="1c46a-104">Exibir dados de cache com Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1c46a-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="1c46a-105">Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspecionar [dados de cache.][MDNCache]</span><span class="sxs-lookup"><span data-stu-id="1c46a-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="1c46a-106">Se você estiver tentando inspecionar dados [de cache HTTP,][MDNHTTPCaching] esse não é o guia que você deseja.</span><span class="sxs-lookup"><span data-stu-id="1c46a-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="1c46a-107">Procure as informações na coluna **Tamanho** do **Log de Rede.**</span><span class="sxs-lookup"><span data-stu-id="1c46a-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="1c46a-108">Navegue até [Log network activity][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="1c46a-108">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <a name="view-cache-data"></a><span data-ttu-id="1c46a-109">Exibir dados de cache</span><span class="sxs-lookup"><span data-stu-id="1c46a-109">View cache data</span></span>  

1.  <span data-ttu-id="1c46a-110">Escolha a **guia Aplicativo** para abrir o **painel Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="1c46a-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="1c46a-111">O **painel** Manifesto geralmente é aberto por padrão.</span><span class="sxs-lookup"><span data-stu-id="1c46a-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="1c46a-113">O **painel** Manifesto</span><span class="sxs-lookup"><span data-stu-id="1c46a-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c46a-114">Expanda **a seção Cache Armazenamento** para exibir caches disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1c46a-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Caches disponíveis" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="1c46a-116">Caches disponíveis</span><span class="sxs-lookup"><span data-stu-id="1c46a-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c46a-117">Escolha um cache para exibir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1c46a-117">Choose a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Exibir o conteúdo de um cache" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="1c46a-119">Exibir o conteúdo de um cache</span><span class="sxs-lookup"><span data-stu-id="1c46a-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c46a-120">Escolha um recurso para exibir os cabeçalhos HTTP na seção abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="1c46a-120">Choose a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Exibir os cabeçalhos HTTP de um recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="1c46a-122">Exibir os cabeçalhos HTTP de um recurso</span><span class="sxs-lookup"><span data-stu-id="1c46a-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c46a-123">Escolha **Visualizar** para exibir o conteúdo de um recurso.</span><span class="sxs-lookup"><span data-stu-id="1c46a-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Exibir o conteúdo de um recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="1c46a-125">Exibir o conteúdo de um recurso</span><span class="sxs-lookup"><span data-stu-id="1c46a-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a><span data-ttu-id="1c46a-126">Atualizar um recurso</span><span class="sxs-lookup"><span data-stu-id="1c46a-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="1c46a-127">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="1c46a-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="1c46a-128">Escolha o recurso que você deseja atualizar.</span><span class="sxs-lookup"><span data-stu-id="1c46a-128">Choose the resource that you want to refresh.</span></span>  <span data-ttu-id="1c46a-129">O DevTools realça-o para indicar que ele está selecionado.</span><span class="sxs-lookup"><span data-stu-id="1c46a-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Escolher um recurso para atualizar" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="1c46a-131">Escolher um recurso para atualizar</span><span class="sxs-lookup"><span data-stu-id="1c46a-131">Choose a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c46a-132">Escolha **Atualizar** \( ![ Atualizar ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1c46a-132">Choose **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\).</span></span>  
    
## <a name="filter-resources"></a><span data-ttu-id="1c46a-133">Filtrar recursos</span><span class="sxs-lookup"><span data-stu-id="1c46a-133">Filter resources</span></span>  

1.  <span data-ttu-id="1c46a-134">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="1c46a-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="1c46a-135">Use a **caixa de texto Filtrar** por Caminho para filtrar todos os recursos que não corresponderem ao caminho que você fornece.</span><span class="sxs-lookup"><span data-stu-id="1c46a-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que não corresponderem ao caminho especificado" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="1c46a-137">Filtrar recursos que não corresponderem ao caminho especificado</span><span class="sxs-lookup"><span data-stu-id="1c46a-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <a name="delete-a-resource"></a><span data-ttu-id="1c46a-138">Excluir um recurso</span><span class="sxs-lookup"><span data-stu-id="1c46a-138">Delete a resource</span></span>  

1.  <span data-ttu-id="1c46a-139">[Exibir os dados de um cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="1c46a-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="1c46a-140">Escolha o recurso que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="1c46a-140">Choose the resource that you want to delete.</span></span>  <span data-ttu-id="1c46a-141">O DevTools realça-o para indicar que ele está selecionado.</span><span class="sxs-lookup"><span data-stu-id="1c46a-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Escolher um recurso a ser excluído" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="1c46a-143">Escolher um recurso a ser excluído</span><span class="sxs-lookup"><span data-stu-id="1c46a-143">Choose a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c46a-144">Escolha **Excluir Selecionado** \( Excluir Selecionado ![ ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1c46a-144">Choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-cache-data"></a><span data-ttu-id="1c46a-145">Excluir todos os dados de cache</span><span class="sxs-lookup"><span data-stu-id="1c46a-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="1c46a-146">Abra **o Aplicativo**Clear  >  **Armazenamento**.</span><span class="sxs-lookup"><span data-stu-id="1c46a-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="1c46a-147">Verifique se a **caixa de Armazenamento** cache está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1c46a-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="A caixa de Armazenamento cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="1c46a-149">A **caixa de Armazenamento** cache</span><span class="sxs-lookup"><span data-stu-id="1c46a-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c46a-150">Escolha **Limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="1c46a-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="O botão Limpar Dados do Site" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="1c46a-152">O **botão Limpar Dados do Site**</span><span class="sxs-lookup"><span data-stu-id="1c46a-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1c46a-153">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1c46a-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Log network activity | Microsoft Docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Armazenamento em cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="1c46a-158">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c46a-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1c46a-159">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/cache) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="1c46a-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1c46a-161">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c46a-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
