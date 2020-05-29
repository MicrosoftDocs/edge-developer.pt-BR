---
title: Exibir recursos de página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611914"
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





# <span data-ttu-id="b495b-103">Exibir recursos de página com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b495b-103">View Page Resources With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="b495b-104">Este guia ensina a usar o Microsoft Edge DevTools para exibir os recursos de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="b495b-104">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="b495b-105">Recursos são os arquivos que uma página precisa para serem exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="b495b-105">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="b495b-106">Exemplos de recursos incluem CSS, JavaScript e arquivos HTML, bem como imagens.</span><span class="sxs-lookup"><span data-stu-id="b495b-106">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="b495b-107">Este guia pressupõe que você esteja familiarizado com as noções básicas de [desenvolvimento da Web][MDNLearnWebDevelopment] e do [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="b495b-107">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="b495b-108">Recursos abertos</span><span class="sxs-lookup"><span data-stu-id="b495b-108">Open resources</span></span>   

<span data-ttu-id="b495b-109">Quando você sabe o nome do recurso que deseja inspecionar, o menu de **comando** fornece uma maneira rápida de abrir o recurso.</span><span class="sxs-lookup"><span data-stu-id="b495b-109">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="b495b-110">Pressione `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="b495b-110">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="b495b-111">A caixa de diálogo **Abrir arquivo** será aberta.</span><span class="sxs-lookup"><span data-stu-id="b495b-111">The **Open File** dialog opens.</span></span>  
    
    > ##### <span data-ttu-id="b495b-112">Figura 1</span><span class="sxs-lookup"><span data-stu-id="b495b-112">Figure 1</span></span>  
    > <span data-ttu-id="b495b-113">A caixa de diálogo **Abrir arquivo**</span><span class="sxs-lookup"><span data-stu-id="b495b-113">The **Open File** dialog</span></span>  
    > ![A caixa de diálogo abrir arquivo][ImageOpenFile]  
    
1.  <span data-ttu-id="b495b-115">Selecione o arquivo na lista suspensa ou comece a digitar o nome do arquivo e pressione `Enter` uma vez que o arquivo correto esteja realçado na caixa preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="b495b-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    > ##### <span data-ttu-id="b495b-116">Figura 2</span><span class="sxs-lookup"><span data-stu-id="b495b-116">Figure 2</span></span>  
    > <span data-ttu-id="b495b-117">Digitando um nome de arquivo na caixa de diálogo **Abrir arquivo**</span><span class="sxs-lookup"><span data-stu-id="b495b-117">Typing a filename in the **Open File** dialog</span></span>  
    > ![Digitando um nome de arquivo na caixa de diálogo abrir arquivo][ImageFileSearch]  
    
### <span data-ttu-id="b495b-119">Recursos abertos no painel rede</span><span class="sxs-lookup"><span data-stu-id="b495b-119">Open resources in the Network panel</span></span>   

<span data-ttu-id="b495b-120">Consulte [inspecionar os detalhes de um recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="b495b-120">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

> ##### <span data-ttu-id="b495b-121">Figura 3</span><span class="sxs-lookup"><span data-stu-id="b495b-121">Figure 3</span></span>  
> <span data-ttu-id="b495b-122">Inspecionar um recurso no painel de rede</span><span class="sxs-lookup"><span data-stu-id="b495b-122">Inspecting a resource in the Network panel</span></span>  
> ![Inspecionar um recurso no painel de rede][ImageNetworkResponse]  

### <span data-ttu-id="b495b-124">Revelar recursos no painel rede de outros painéis</span><span class="sxs-lookup"><span data-stu-id="b495b-124">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="b495b-125">A seção [procurar recursos](#browse-resources) abaixo mostra como exibir recursos de várias partes da interface do usuário do devtools.</span><span class="sxs-lookup"><span data-stu-id="b495b-125">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="b495b-126">Se você quiser inspecionar um recurso no painel de **rede** , clique com o botão direito do mouse no recurso e selecione **revelar no painel de rede**.</span><span class="sxs-lookup"><span data-stu-id="b495b-126">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

> ##### <span data-ttu-id="b495b-127">Figura 4</span><span class="sxs-lookup"><span data-stu-id="b495b-127">Figure 4</span></span>  
> <span data-ttu-id="b495b-128">A opção **revelar no painel de rede**</span><span class="sxs-lookup"><span data-stu-id="b495b-128">The **Reveal in Network panel** option</span></span>  
> ![Revelar no painel de rede][ImageRevealNetwork]  

## <span data-ttu-id="b495b-130">Procurar recursos</span><span class="sxs-lookup"><span data-stu-id="b495b-130">Browse resources</span></span>   

### <span data-ttu-id="b495b-131">Procurar recursos no painel rede</span><span class="sxs-lookup"><span data-stu-id="b495b-131">Browse resources in the Network panel</span></span>   

<span data-ttu-id="b495b-132">Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="b495b-132">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

> ##### <span data-ttu-id="b495b-133">Figura 5</span><span class="sxs-lookup"><span data-stu-id="b495b-133">Figure 5</span></span>  
> <span data-ttu-id="b495b-134">Recursos de página no log de rede</span><span class="sxs-lookup"><span data-stu-id="b495b-134">Page resources in the Network Log</span></span>  
> ![Recursos de página no log de rede][ImageNetworkLog]  

### <span data-ttu-id="b495b-136">Navegar por diretório</span><span class="sxs-lookup"><span data-stu-id="b495b-136">Browse by directory</span></span>   

<span data-ttu-id="b495b-137">Para exibir os recursos de uma página organizada por diretório:</span><span class="sxs-lookup"><span data-stu-id="b495b-137">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="b495b-138">Clique na guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="b495b-138">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="b495b-139">Clique na guia **página** para mostrar os recursos da página.</span><span class="sxs-lookup"><span data-stu-id="b495b-139">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="b495b-140">O painel da **página** é aberto.</span><span class="sxs-lookup"><span data-stu-id="b495b-140">The **Page** pane opens.</span></span>  
    
    > ##### <span data-ttu-id="b495b-141">Figura 6</span><span class="sxs-lookup"><span data-stu-id="b495b-141">Figure 6</span></span>  
    > <span data-ttu-id="b495b-142">Painel de **página**</span><span class="sxs-lookup"><span data-stu-id="b495b-142">The **Page** pane</span></span>  
    > ![Painel de página][ImagePage]  
    
    <span data-ttu-id="b495b-144">Aqui está um detalhamento dos itens não óbvios na [Figura 6](#figure-6):</span><span class="sxs-lookup"><span data-stu-id="b495b-144">Here is a breakdown of the non-obvious items in [Figure 6](#figure-6):</span></span>  
    
    | <span data-ttu-id="b495b-145">Item de página</span><span class="sxs-lookup"><span data-stu-id="b495b-145">Page item</span></span> | <span data-ttu-id="b495b-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="b495b-146">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="b495b-147">O contexto de [navegação][MDNInlineFrame]do documento principal.</span><span class="sxs-lookup"><span data-stu-id="b495b-147">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="b495b-148">O domínio.</span><span class="sxs-lookup"><span data-stu-id="b495b-148">The domain.</span></span>  <span data-ttu-id="b495b-149">Todos os recursos aninhados nela vêm desse domínio.</span><span class="sxs-lookup"><span data-stu-id="b495b-149">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="b495b-150">Por exemplo, a URL completa do `comlink.global.j` arquivo é provavelmente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="b495b-150">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="b495b-151">Um diretório.</span><span class="sxs-lookup"><span data-stu-id="b495b-151">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="b495b-152">O documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="b495b-152">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="b495b-153">Um contexto do tempo de execução do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="b495b-153">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="b495b-154">Clique em um recurso para exibi-lo no **Editor**.</span><span class="sxs-lookup"><span data-stu-id="b495b-154">Click a resource to view it in the **Editor**.</span></span>  
    
    > ##### <span data-ttu-id="b495b-155">Figura 7</span><span class="sxs-lookup"><span data-stu-id="b495b-155">Figure 7</span></span>  
    > <span data-ttu-id="b495b-156">Exibir um arquivo no **Editor**</span><span class="sxs-lookup"><span data-stu-id="b495b-156">Viewing a file in the **Editor**</span></span>  
    > ![Exibir um arquivo no editor][ImageSourcesView]  
    
### <span data-ttu-id="b495b-158">Procurar por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="b495b-158">Browse by filename</span></span>   

<span data-ttu-id="b495b-159">Por padrão, o painel de **página** agrupa os recursos por diretório.</span><span class="sxs-lookup"><span data-stu-id="b495b-159">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="b495b-160">Para desabilitar esse agrupamento e exibir os recursos de cada domínio como uma lista plana:</span><span class="sxs-lookup"><span data-stu-id="b495b-160">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="b495b-161">Abrir o painel da **página** .</span><span class="sxs-lookup"><span data-stu-id="b495b-161">Open the **Page** pane.</span></span>  <span data-ttu-id="b495b-162">Consulte [procurar por diretório](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="b495b-162">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="b495b-163">Clique em **mais opções** `...` e desabilite **Agrupar por pasta**.</span><span class="sxs-lookup"><span data-stu-id="b495b-163">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    > ##### <span data-ttu-id="b495b-164">Figura 8</span><span class="sxs-lookup"><span data-stu-id="b495b-164">Figure 8</span></span>  
    > <span data-ttu-id="b495b-165">A opção **Agrupar por pasta**</span><span class="sxs-lookup"><span data-stu-id="b495b-165">The **Group By Folder** option</span></span>  
    > ![A opção Agrupar por pasta][ImageGroupByFolder]  
    
    <span data-ttu-id="b495b-167">Os recursos são organizados por tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b495b-167">Resources are organized by file type.</span></span>  <span data-ttu-id="b495b-168">Em cada tipo de arquivo, os recursos são organizados em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="b495b-168">Within each file type the resources are organized alphabetically.</span></span>  
    
    > ##### <span data-ttu-id="b495b-169">Figura 9</span><span class="sxs-lookup"><span data-stu-id="b495b-169">Figure 9</span></span>  
    > <span data-ttu-id="b495b-170">O painel da **página** depois de desabilitar **Agrupar por pasta**</span><span class="sxs-lookup"><span data-stu-id="b495b-170">The **Page** pane after disabling **Group By Folder**</span></span>  
    > ![O painel da página depois de desabilitar agrupar por pasta][ImageFileNames]  
    
### <span data-ttu-id="b495b-172">Procurar por tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="b495b-172">Browse by file type</span></span>   

<span data-ttu-id="b495b-173">Para agrupar recursos juntamente com base no tipo de arquivo:</span><span class="sxs-lookup"><span data-stu-id="b495b-173">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="b495b-174">Clique na guia **aplicativo** .  O painel **aplicativo** é aberto.</span><span class="sxs-lookup"><span data-stu-id="b495b-174">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="b495b-175">Por padrão, o painel de **manifesto** geralmente abre primeiro.</span><span class="sxs-lookup"><span data-stu-id="b495b-175">By default the **Manifest** pane usually opens first.</span></span>  
    
    > ##### <span data-ttu-id="b495b-176">Figura 10</span><span class="sxs-lookup"><span data-stu-id="b495b-176">Figure 10</span></span>  
    > <span data-ttu-id="b495b-177">Painel de **aplicativos**</span><span class="sxs-lookup"><span data-stu-id="b495b-177">The **Application** panel</span></span>  
    > ![Painel de aplicativos][ImageApplication]  
    
1.  <span data-ttu-id="b495b-179">Role para baixo até o painel **quadros** .</span><span class="sxs-lookup"><span data-stu-id="b495b-179">Scroll down to the **Frames** pane.</span></span>  
    
    > ##### <span data-ttu-id="b495b-180">Figura 11</span><span class="sxs-lookup"><span data-stu-id="b495b-180">Figure 11</span></span>  
    > <span data-ttu-id="b495b-181">O painel **quadros**</span><span class="sxs-lookup"><span data-stu-id="b495b-181">The **Frames** pane</span></span>  
    > ![O painel quadros][ImageFrames]  
    
1.  <span data-ttu-id="b495b-183">Expanda as seções em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="b495b-183">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="b495b-184">Clique em um recurso para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="b495b-184">Click a resource to view it.</span></span>  
    
    > ##### <span data-ttu-id="b495b-185">Figura 12</span><span class="sxs-lookup"><span data-stu-id="b495b-185">Figure 12</span></span>  
    > <span data-ttu-id="b495b-186">Exibindo um recurso no painel do **aplicativo**</span><span class="sxs-lookup"><span data-stu-id="b495b-186">Viewing a resource in the **Application** panel</span></span>  
    > ![Exibindo um recurso no painel do aplicativo][ImageApplicationView]  

#### <span data-ttu-id="b495b-188">Procurar arquivos por tipo no painel rede</span><span class="sxs-lookup"><span data-stu-id="b495b-188">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="b495b-189">Consulte [Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="b495b-189">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

> ##### <span data-ttu-id="b495b-190">Figura 13</span><span class="sxs-lookup"><span data-stu-id="b495b-190">Figure 13</span></span>  
> <span data-ttu-id="b495b-191">Filtragem de CSS no log de rede</span><span class="sxs-lookup"><span data-stu-id="b495b-191">Filtering for CSS in the Network Log</span></span>  
> ![Filtragem de CSS no log de rede][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Figura 1: caixa de diálogo abrir arquivo"  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Figura 2: digitando um nome de arquivo na caixa de diálogo abrir arquivo"  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Figura 3: inspecionando um recurso no painel * * Network * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Figura 4: revelar no painel de rede"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Figura 5: recursos de página no log de rede"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Figura 6: o painel da página"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Figura 7: exibindo um arquivo no editor"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Figura 8: a opção Agrupar por pasta"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Figura 9: painel da página depois de desabilitar agrupar por pasta"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Figura 10: o painel do aplicativo"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Figura 11: o painel quadros"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Figura 12: exibindo um recurso no painel do aplicativo"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Figura 13: filtragem para CSS no log de rede"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Filtrar por tipo de recurso-inspecionar atividade de rede no Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecionar os detalhes da atividade de rede de inspeção de recursos no Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar atividades de rede-Inspecione a atividade de rede no Microsoft Edge DevTools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "> de<iframe: o elemento frame embutido | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprender sobre desenvolvimento na Web | MDN"  

> [!NOTE]
> <span data-ttu-id="b495b-212">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="b495b-212">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b495b-213">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/resources/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b495b-213">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b495b-215">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b495b-215">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
