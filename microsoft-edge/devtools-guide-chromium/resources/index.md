---
description: Organize recursos por quadro, domínio, tipo ou outros critérios.
title: Exibir recursos de página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 353c36a9d98dac287c3fdaaa3feed2fe3b17cd07
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230772"
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

# <span data-ttu-id="5d47c-104">Exibir recursos de página com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5d47c-104">View page resources with Microsoft Edge DevTools</span></span>  

  

<span data-ttu-id="5d47c-105">Este guia ensina a usar o Microsoft Edge DevTools para exibir os recursos de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="5d47c-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="5d47c-106">Recursos são os arquivos que uma página precisa para serem exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d47c-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="5d47c-107">Exemplos de recursos incluem CSS, JavaScript e arquivos HTML, bem como imagens.</span><span class="sxs-lookup"><span data-stu-id="5d47c-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="5d47c-108">Este guia pressupõe que você esteja familiarizado com as noções básicas de [desenvolvimento da Web][MDNLearnWebDevelopment] e do [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="5d47c-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="5d47c-109">Recursos abertos</span><span class="sxs-lookup"><span data-stu-id="5d47c-109">Open resources</span></span>  

<span data-ttu-id="5d47c-110">Quando você sabe o nome do recurso que deseja inspecionar, o menu de **comando** fornece uma maneira rápida de abrir o recurso.</span><span class="sxs-lookup"><span data-stu-id="5d47c-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="5d47c-111">Selecione `Control` + `P` \ (Windows, Linux \) ou `Command` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="5d47c-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="5d47c-112">A caixa de diálogo **Abrir arquivo** será aberta.</span><span class="sxs-lookup"><span data-stu-id="5d47c-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="A caixa de diálogo abrir arquivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="5d47c-114">A caixa de diálogo **Abrir arquivo**</span><span class="sxs-lookup"><span data-stu-id="5d47c-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5d47c-115">Selecione o arquivo na lista suspensa ou comece a digitar o nome do arquivo e selecione `Enter` uma vez que o arquivo correto seja realçado na caixa preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="5d47c-115">Select the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Digite um nome de arquivo na caixa de diálogo abrir arquivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="5d47c-117">Digite um nome de arquivo na caixa de diálogo **Abrir arquivo**</span><span class="sxs-lookup"><span data-stu-id="5d47c-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="5d47c-118">Recursos abertos no painel rede</span><span class="sxs-lookup"><span data-stu-id="5d47c-118">Open resources in the Network panel</span></span>  

<span data-ttu-id="5d47c-119">Navegue para [inspecionar os detalhes de um recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="5d47c-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecionar um recurso no painel de rede" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="5d47c-121">Inspecionar um recurso no painel de **rede**</span><span class="sxs-lookup"><span data-stu-id="5d47c-121">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="5d47c-122">Revelar recursos no painel rede de outros painéis</span><span class="sxs-lookup"><span data-stu-id="5d47c-122">Reveal resources in the Network panel from other panels</span></span>  

<span data-ttu-id="5d47c-123">A seção [procurar recursos](#browse-resources) abaixo mostra como exibir recursos de várias partes da interface do usuário do devtools.</span><span class="sxs-lookup"><span data-stu-id="5d47c-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="5d47c-124">Se você quiser inspecionar um recurso no painel de **rede** , clique com o botão direito do mouse no recurso e escolha **revelar no painel de rede**.</span><span class="sxs-lookup"><span data-stu-id="5d47c-124">If you ever want to inspect a resource in the **Network** panel, right-click the resource and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Revelar no painel de rede" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="5d47c-126">Revelar no painel de rede</span><span class="sxs-lookup"><span data-stu-id="5d47c-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="5d47c-127">Procurar recursos</span><span class="sxs-lookup"><span data-stu-id="5d47c-127">Browse resources</span></span>  

### <span data-ttu-id="5d47c-128">Procurar recursos no painel rede</span><span class="sxs-lookup"><span data-stu-id="5d47c-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="5d47c-129">Navegue até [registrar atividades de rede][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="5d47c-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página no log de rede" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="5d47c-131">Recursos de página no log de **rede**</span><span class="sxs-lookup"><span data-stu-id="5d47c-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="5d47c-132">Navegar por diretório</span><span class="sxs-lookup"><span data-stu-id="5d47c-132">Browse by directory</span></span>  

<span data-ttu-id="5d47c-133">Para exibir os recursos de uma página organizada por diretório:</span><span class="sxs-lookup"><span data-stu-id="5d47c-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="5d47c-134">Clique na guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="5d47c-134">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="5d47c-135">Clique na guia **página** para mostrar os recursos da página.</span><span class="sxs-lookup"><span data-stu-id="5d47c-135">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="5d47c-136">O painel da **página** é aberto.</span><span class="sxs-lookup"><span data-stu-id="5d47c-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Painel de página" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="5d47c-138">Painel de **página**</span><span class="sxs-lookup"><span data-stu-id="5d47c-138">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="5d47c-139">Aqui está um detalhamento dos itens não óbvios na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="5d47c-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="5d47c-140">Item de página</span><span class="sxs-lookup"><span data-stu-id="5d47c-140">Page item</span></span> | <span data-ttu-id="5d47c-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d47c-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="5d47c-142">O contexto de [navegação][MDNInlineFrame]do documento principal.</span><span class="sxs-lookup"><span data-stu-id="5d47c-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="5d47c-143">O domínio.</span><span class="sxs-lookup"><span data-stu-id="5d47c-143">The domain.</span></span>  <span data-ttu-id="5d47c-144">Todos os recursos aninhados nela vêm desse domínio.</span><span class="sxs-lookup"><span data-stu-id="5d47c-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="5d47c-145">Por exemplo, a URL completa do `comlink.global.j` arquivo é provavelmente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="5d47c-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="5d47c-146">Um diretório.</span><span class="sxs-lookup"><span data-stu-id="5d47c-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="5d47c-147">O documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="5d47c-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="5d47c-148">Um contexto do tempo de execução do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="5d47c-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="5d47c-149">Clique em um recurso para exibi-lo no **Editor**.</span><span class="sxs-lookup"><span data-stu-id="5d47c-149">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Exibir um arquivo no editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="5d47c-151">Exibir um arquivo no **Editor**</span><span class="sxs-lookup"><span data-stu-id="5d47c-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="5d47c-152">Procurar por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="5d47c-152">Browse by filename</span></span>  

<span data-ttu-id="5d47c-153">Por padrão, o painel de **página** agrupa os recursos por diretório.</span><span class="sxs-lookup"><span data-stu-id="5d47c-153">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="5d47c-154">Para desabilitar esse agrupamento e exibir os recursos de cada domínio como uma lista plana:</span><span class="sxs-lookup"><span data-stu-id="5d47c-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="5d47c-155">Abrir o painel da **página** .</span><span class="sxs-lookup"><span data-stu-id="5d47c-155">Open the **Page** pane.</span></span>  <span data-ttu-id="5d47c-156">Navegue até [navegar por diretório](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="5d47c-156">Navigate to [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="5d47c-157">Escolha **mais opções** `...` e desabilite **Agrupar por pasta**.</span><span class="sxs-lookup"><span data-stu-id="5d47c-157">Choose **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="A opção Agrupar por pasta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="5d47c-159">A opção **Agrupar por pasta**</span><span class="sxs-lookup"><span data-stu-id="5d47c-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="5d47c-160">Os recursos são organizados por tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d47c-160">Resources are organized by file type.</span></span>  <span data-ttu-id="5d47c-161">Em cada tipo de arquivo, os recursos são organizados em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="5d47c-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="O painel da página depois de desabilitar agrupar por pasta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="5d47c-163">O painel da **página** depois de desabilitar **Agrupar por pasta**</span><span class="sxs-lookup"><span data-stu-id="5d47c-163">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="5d47c-164">Procurar por tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="5d47c-164">Browse by file type</span></span>  

<span data-ttu-id="5d47c-165">Para agrupar recursos juntamente com base no tipo de arquivo:</span><span class="sxs-lookup"><span data-stu-id="5d47c-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="5d47c-166">Clique na guia **aplicativo** .  O painel **aplicativo** é aberto.</span><span class="sxs-lookup"><span data-stu-id="5d47c-166">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="5d47c-167">Por padrão, o painel de **manifesto** geralmente abre primeiro.</span><span class="sxs-lookup"><span data-stu-id="5d47c-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Painel de aplicativos" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="5d47c-169">Painel de **aplicativos**</span><span class="sxs-lookup"><span data-stu-id="5d47c-169">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5d47c-170">Role para baixo até o painel **quadros** .</span><span class="sxs-lookup"><span data-stu-id="5d47c-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="O painel quadros" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="5d47c-172">O painel **quadros**</span><span class="sxs-lookup"><span data-stu-id="5d47c-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5d47c-173">Expanda as seções em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="5d47c-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="5d47c-174">Clique em um recurso para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="5d47c-174">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Exibir um recurso no painel do aplicativo" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="5d47c-176">Exibir um recurso no painel do **aplicativo**</span><span class="sxs-lookup"><span data-stu-id="5d47c-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="5d47c-177">Procurar arquivos por tipo no painel rede</span><span class="sxs-lookup"><span data-stu-id="5d47c-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="5d47c-178">Navegue até [Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="5d47c-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtro para CSS no log de rede" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="5d47c-180">Filtro para CSS no log de **rede**</span><span class="sxs-lookup"><span data-stu-id="5d47c-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <span data-ttu-id="5d47c-181">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5d47c-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso-inspecionar atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecionar os detalhes da atividade de rede de inspeção de recursos no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Registrar atividades de rede-Inspecione a atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "> de<iframe: o elemento frame embutido | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprender sobre desenvolvimento na Web | MDN"  

> [!NOTE]
> <span data-ttu-id="5d47c-188">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d47c-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5d47c-189">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/resources/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5d47c-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5d47c-191">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d47c-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
