---
description: Organize recursos por quadro, domínio, tipo ou outros critérios.
title: Exibir recursos de página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4f90927cc4044c722d9a62ab4b0427aa2753e4c5
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993587"
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





# <span data-ttu-id="aae0a-104">Exibir recursos de página com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aae0a-104">View page resources with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="aae0a-105">Este guia ensina a usar o Microsoft Edge DevTools para exibir os recursos de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="aae0a-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="aae0a-106">Recursos são os arquivos que uma página precisa para serem exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="aae0a-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="aae0a-107">Exemplos de recursos incluem CSS, JavaScript e arquivos HTML, bem como imagens.</span><span class="sxs-lookup"><span data-stu-id="aae0a-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="aae0a-108">Este guia pressupõe que você esteja familiarizado com as noções básicas de [desenvolvimento da Web][MDNLearnWebDevelopment] e do [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="aae0a-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="aae0a-109">Recursos abertos</span><span class="sxs-lookup"><span data-stu-id="aae0a-109">Open resources</span></span>   

<span data-ttu-id="aae0a-110">Quando você sabe o nome do recurso que deseja inspecionar, o menu de **comando** fornece uma maneira rápida de abrir o recurso.</span><span class="sxs-lookup"><span data-stu-id="aae0a-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="aae0a-111">Pressione `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="aae0a-111">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="aae0a-112">A caixa de diálogo **Abrir arquivo** será aberta.</span><span class="sxs-lookup"><span data-stu-id="aae0a-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="A caixa de diálogo abrir arquivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="aae0a-114">A caixa de diálogo **Abrir arquivo**</span><span class="sxs-lookup"><span data-stu-id="aae0a-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aae0a-115">Selecione o arquivo na lista suspensa ou comece a digitar o nome do arquivo e pressione `Enter` uma vez que o arquivo correto esteja realçado na caixa preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="aae0a-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Digite um nome de arquivo na caixa de diálogo abrir arquivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="aae0a-117">Digite um nome de arquivo na caixa de diálogo **Abrir arquivo**</span><span class="sxs-lookup"><span data-stu-id="aae0a-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="aae0a-118">Recursos abertos no painel rede</span><span class="sxs-lookup"><span data-stu-id="aae0a-118">Open resources in the Network panel</span></span>   

<span data-ttu-id="aae0a-119">Consulte [inspecionar os detalhes de um recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="aae0a-119">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecionar um recurso no painel de rede" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="aae0a-121">Inspecionar um recurso no painel de **rede**</span><span class="sxs-lookup"><span data-stu-id="aae0a-121">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="aae0a-122">Revelar recursos no painel rede de outros painéis</span><span class="sxs-lookup"><span data-stu-id="aae0a-122">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="aae0a-123">A seção [procurar recursos](#browse-resources) abaixo mostra como exibir recursos de várias partes da interface do usuário do devtools.</span><span class="sxs-lookup"><span data-stu-id="aae0a-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="aae0a-124">Se você quiser inspecionar um recurso no painel de **rede** , clique com o botão direito do mouse no recurso e selecione **revelar no painel de rede**.</span><span class="sxs-lookup"><span data-stu-id="aae0a-124">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Revelar no painel de rede" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="aae0a-126">Revelar no painel de rede</span><span class="sxs-lookup"><span data-stu-id="aae0a-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="aae0a-127">Procurar recursos</span><span class="sxs-lookup"><span data-stu-id="aae0a-127">Browse resources</span></span>   

### <span data-ttu-id="aae0a-128">Procurar recursos no painel rede</span><span class="sxs-lookup"><span data-stu-id="aae0a-128">Browse resources in the Network panel</span></span>   

<span data-ttu-id="aae0a-129">Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="aae0a-129">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página no log de rede" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="aae0a-131">Recursos de página no log de **rede**</span><span class="sxs-lookup"><span data-stu-id="aae0a-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="aae0a-132">Navegar por diretório</span><span class="sxs-lookup"><span data-stu-id="aae0a-132">Browse by directory</span></span>   

<span data-ttu-id="aae0a-133">Para exibir os recursos de uma página organizada por diretório:</span><span class="sxs-lookup"><span data-stu-id="aae0a-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="aae0a-134">Clique na guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="aae0a-134">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="aae0a-135">Clique na guia **página** para mostrar os recursos da página.</span><span class="sxs-lookup"><span data-stu-id="aae0a-135">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="aae0a-136">O painel da **página** é aberto.</span><span class="sxs-lookup"><span data-stu-id="aae0a-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Painel de página" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="aae0a-138">Painel de **página**</span><span class="sxs-lookup"><span data-stu-id="aae0a-138">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="aae0a-139">Aqui está um detalhamento dos itens não óbvios na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="aae0a-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="aae0a-140">Item de página</span><span class="sxs-lookup"><span data-stu-id="aae0a-140">Page item</span></span> | <span data-ttu-id="aae0a-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="aae0a-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="aae0a-142">O contexto de [navegação][MDNInlineFrame]do documento principal.</span><span class="sxs-lookup"><span data-stu-id="aae0a-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="aae0a-143">O domínio.</span><span class="sxs-lookup"><span data-stu-id="aae0a-143">The domain.</span></span>  <span data-ttu-id="aae0a-144">Todos os recursos aninhados nela vêm desse domínio.</span><span class="sxs-lookup"><span data-stu-id="aae0a-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="aae0a-145">Por exemplo, a URL completa do `comlink.global.j` arquivo é provavelmente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="aae0a-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="aae0a-146">Um diretório.</span><span class="sxs-lookup"><span data-stu-id="aae0a-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="aae0a-147">O documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="aae0a-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="aae0a-148">Um contexto do tempo de execução do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="aae0a-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="aae0a-149">Clique em um recurso para exibi-lo no **Editor**.</span><span class="sxs-lookup"><span data-stu-id="aae0a-149">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Exibir um arquivo no editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="aae0a-151">Exibir um arquivo no **Editor**</span><span class="sxs-lookup"><span data-stu-id="aae0a-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="aae0a-152">Procurar por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="aae0a-152">Browse by filename</span></span>   

<span data-ttu-id="aae0a-153">Por padrão, o painel de **página** agrupa os recursos por diretório.</span><span class="sxs-lookup"><span data-stu-id="aae0a-153">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="aae0a-154">Para desabilitar esse agrupamento e exibir os recursos de cada domínio como uma lista plana:</span><span class="sxs-lookup"><span data-stu-id="aae0a-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="aae0a-155">Abrir o painel da **página** .</span><span class="sxs-lookup"><span data-stu-id="aae0a-155">Open the **Page** pane.</span></span>  <span data-ttu-id="aae0a-156">Consulte [procurar por diretório](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="aae0a-156">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="aae0a-157">Clique em **mais opções** `...` e desabilite **Agrupar por pasta**.</span><span class="sxs-lookup"><span data-stu-id="aae0a-157">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="A opção Agrupar por pasta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="aae0a-159">A opção **Agrupar por pasta**</span><span class="sxs-lookup"><span data-stu-id="aae0a-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="aae0a-160">Os recursos são organizados por tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="aae0a-160">Resources are organized by file type.</span></span>  <span data-ttu-id="aae0a-161">Em cada tipo de arquivo, os recursos são organizados em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="aae0a-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="O painel da página depois de desabilitar agrupar por pasta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="aae0a-163">O painel da **página** depois de desabilitar **Agrupar por pasta**</span><span class="sxs-lookup"><span data-stu-id="aae0a-163">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="aae0a-164">Procurar por tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="aae0a-164">Browse by file type</span></span>   

<span data-ttu-id="aae0a-165">Para agrupar recursos juntamente com base no tipo de arquivo:</span><span class="sxs-lookup"><span data-stu-id="aae0a-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="aae0a-166">Clique na guia **aplicativo** .  O painel **aplicativo** é aberto.</span><span class="sxs-lookup"><span data-stu-id="aae0a-166">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="aae0a-167">Por padrão, o painel de **manifesto** geralmente abre primeiro.</span><span class="sxs-lookup"><span data-stu-id="aae0a-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Painel de aplicativos" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="aae0a-169">Painel de **aplicativos**</span><span class="sxs-lookup"><span data-stu-id="aae0a-169">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aae0a-170">Role para baixo até o painel **quadros** .</span><span class="sxs-lookup"><span data-stu-id="aae0a-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="O painel quadros" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="aae0a-172">O painel **quadros**</span><span class="sxs-lookup"><span data-stu-id="aae0a-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aae0a-173">Expanda as seções em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="aae0a-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="aae0a-174">Clique em um recurso para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="aae0a-174">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Exibir um recurso no painel do aplicativo" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="aae0a-176">Exibir um recurso no painel do **aplicativo**</span><span class="sxs-lookup"><span data-stu-id="aae0a-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="aae0a-177">Procurar arquivos por tipo no painel rede</span><span class="sxs-lookup"><span data-stu-id="aae0a-177">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="aae0a-178">Consulte [Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="aae0a-178">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtro para CSS no log de rede" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="aae0a-180">Filtro para CSS no log de **rede**</span><span class="sxs-lookup"><span data-stu-id="aae0a-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso-inspecionar atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecionar os detalhes da atividade de rede de inspeção de recursos no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Registrar atividades de rede-Inspecione a atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "> de<iframe: o elemento frame embutido | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprender sobre desenvolvimento na Web | MDN"  

> [!NOTE]
> <span data-ttu-id="aae0a-187">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="aae0a-187">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aae0a-188">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/resources/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="aae0a-188">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aae0a-190">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aae0a-190">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
