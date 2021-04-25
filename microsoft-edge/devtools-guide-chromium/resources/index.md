---
description: Organize recursos por quadro, domínio, tipo ou outros critérios.
title: Exibir recursos de página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 818b93c1c07a93baa8972a530871d20446fd687f
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519440"
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

# <a name="view-page-resources-with-microsoft-edge-devtools"></a><span data-ttu-id="52f83-104">Exibir recursos de página com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="52f83-104">View page resources with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="52f83-105">Este guia ensina como usar o Microsoft Edge DevTools para exibir os recursos de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="52f83-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="52f83-106">Recursos são os arquivos que uma página precisa para exibir corretamente.</span><span class="sxs-lookup"><span data-stu-id="52f83-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="52f83-107">Exemplos de recursos incluem arquivos CSS, JavaScript e HTML, bem como imagens.</span><span class="sxs-lookup"><span data-stu-id="52f83-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="52f83-108">Este guia supõe que você está familiarizado com os conceitos básicos de [desenvolvimento da Web][MDNLearnWebDevelopment] e Microsoft Edge [DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="52f83-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-resources"></a><span data-ttu-id="52f83-109">Abrir recursos</span><span class="sxs-lookup"><span data-stu-id="52f83-109">Open resources</span></span>  

<span data-ttu-id="52f83-110">Quando você sabe o nome do recurso que deseja inspecionar, o **Menu de Comando** fornece uma maneira rápida de abrir o recurso.</span><span class="sxs-lookup"><span data-stu-id="52f83-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="52f83-111">Selecione `Control` + `P` \(Windows, Linux\) `Command` + `P` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="52f83-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="52f83-112">A **caixa de diálogo** Abrir Arquivo é aberta.</span><span class="sxs-lookup"><span data-stu-id="52f83-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="A caixa de diálogo Abrir Arquivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="52f83-114">A **caixa de diálogo Abrir Arquivo**</span><span class="sxs-lookup"><span data-stu-id="52f83-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52f83-115">Escolha o arquivo no menu suspenso ou comece a digitar o nome do arquivo e selecione quando o arquivo correto for realçado na caixa de preenchimento `Enter` automático.</span><span class="sxs-lookup"><span data-stu-id="52f83-115">Choose the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Digite um nome de arquivo na caixa de diálogo Abrir Arquivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="52f83-117">Digite um nome de arquivo na caixa **de diálogo Abrir Arquivo**</span><span class="sxs-lookup"><span data-stu-id="52f83-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a><span data-ttu-id="52f83-118">Abrir recursos na ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="52f83-118">Open resources in the Network tool</span></span>  

<span data-ttu-id="52f83-119">Navegue [até Inspecionar os detalhes de um recurso][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="52f83-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecionar um recurso na ferramenta Rede" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="52f83-121">Inspecionar um recurso na **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="52f83-121">Inspect a resource in the **Network** tool</span></span>  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a><span data-ttu-id="52f83-122">Revelar recursos na ferramenta Rede de outros painéis</span><span class="sxs-lookup"><span data-stu-id="52f83-122">Reveal resources in the Network tool from other panels</span></span>  

<span data-ttu-id="52f83-123">A [seção Procurar recursos](#browse-resources) abaixo mostra como exibir recursos de várias partes da interface do usuário do DevTools.</span><span class="sxs-lookup"><span data-stu-id="52f83-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="52f83-124">Se você quiser inspecionar um \*\*\*\* recurso na ferramenta Rede, passe o mouse no recurso, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Revelar no painel Rede.**</span><span class="sxs-lookup"><span data-stu-id="52f83-124">If you ever want to inspect a resource in the **Network** tool,  hover on the resource, open the contextual menu \(right-click\), and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Revelação no painel Rede" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="52f83-126">Revelação no painel Rede</span><span class="sxs-lookup"><span data-stu-id="52f83-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <a name="browse-resources"></a><span data-ttu-id="52f83-127">Procurar recursos</span><span class="sxs-lookup"><span data-stu-id="52f83-127">Browse resources</span></span>  

### <a name="browse-resources-in-the-network-panel"></a><span data-ttu-id="52f83-128">Procurar recursos no painel Rede</span><span class="sxs-lookup"><span data-stu-id="52f83-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="52f83-129">Navegue até [Log network activity][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="52f83-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página no Log de Rede" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="52f83-131">Recursos de página no Log **de** Rede</span><span class="sxs-lookup"><span data-stu-id="52f83-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <a name="browse-by-directory"></a><span data-ttu-id="52f83-132">Procurar por diretório</span><span class="sxs-lookup"><span data-stu-id="52f83-132">Browse by directory</span></span>  

<span data-ttu-id="52f83-133">Para exibir os recursos de uma página da Web organizada pelo diretório:</span><span class="sxs-lookup"><span data-stu-id="52f83-133">To view the resources of a webpage organized by directory:</span></span>  

1.  <span data-ttu-id="52f83-134">Abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="52f83-134">Open DevTools.</span></span>
1.  <span data-ttu-id="52f83-135">Escolha a **ferramenta Fontes** e, no painel **Navegador,** no canto superior esquerdo, escolha a **guia** Página.</span><span class="sxs-lookup"><span data-stu-id="52f83-135">Choose the **Sources** tool, and then in the **Navigator** pane in the upper left, choose the **Page** tab.</span></span>
1.  <span data-ttu-id="52f83-136">Escolha o **botão Mais opções** (...) à direita da guia **Página** e escolha Grupo **por pasta**.</span><span class="sxs-lookup"><span data-stu-id="52f83-136">Choose the **More options** (...) button to the right of the **Page** tab, and then choose **Group by folder**.</span></span>
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="A guia Página no painel Navegador da ferramenta Sources" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="52f83-138">A **guia Página** no painel **Navegador** da ferramenta **Sources**</span><span class="sxs-lookup"><span data-stu-id="52f83-138">The **Page** tab in the **Navigator** pane of the **Sources** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="52f83-139">Aqui está uma divisão dos itens não óbvios na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="52f83-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="52f83-140">Item de página</span><span class="sxs-lookup"><span data-stu-id="52f83-140">Page item</span></span> | <span data-ttu-id="52f83-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="52f83-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="52f83-142">O contexto principal [de navegação do documento.][MDNInlineFrame]</span><span class="sxs-lookup"><span data-stu-id="52f83-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="52f83-143">O domínio.</span><span class="sxs-lookup"><span data-stu-id="52f83-143">The domain.</span></span>  <span data-ttu-id="52f83-144">Todos os recursos aninhados sob ele vêm desse domínio.</span><span class="sxs-lookup"><span data-stu-id="52f83-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="52f83-145">Por exemplo, a URL completa do `comlink.global.j` arquivo é provavelmente `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="52f83-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="52f83-146">Um diretório.</span><span class="sxs-lookup"><span data-stu-id="52f83-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="52f83-147">O documento HTML principal.</span><span class="sxs-lookup"><span data-stu-id="52f83-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="52f83-148">Um contexto de tempo de execução do trabalhador de serviço.</span><span class="sxs-lookup"><span data-stu-id="52f83-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="52f83-149">Escolha um recurso para exibi-lo no **Editor**.</span><span class="sxs-lookup"><span data-stu-id="52f83-149">Choose a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Exibir um arquivo no Editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="52f83-151">Exibir um arquivo no **Editor**</span><span class="sxs-lookup"><span data-stu-id="52f83-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <a name="browse-by-filename"></a><span data-ttu-id="52f83-152">Procurar por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="52f83-152">Browse by filename</span></span>  

<span data-ttu-id="52f83-153">Por padrão, a guia **Página** grupos recursos por diretório.</span><span class="sxs-lookup"><span data-stu-id="52f83-153">By default, the **Page** tab groups resources by directory.</span></span>  <span data-ttu-id="52f83-154">Para exibir os recursos de cada domínio como uma lista simples, em vez de a agrupar por diretório:</span><span class="sxs-lookup"><span data-stu-id="52f83-154">To display the resources for each domain as a flat list, instead of grouping them by directory:</span></span>

1.  <span data-ttu-id="52f83-155">Navegue até a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="52f83-155">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="52f83-156">No painel **Navegador** (à esquerda), escolha a **guia** Página.</span><span class="sxs-lookup"><span data-stu-id="52f83-156">In the **Navigator** pane (on the left), choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="52f83-157">Escolha **Mais opções** e `...` desmarca a marca de seleção ao lado de **Grupo por pasta**.</span><span class="sxs-lookup"><span data-stu-id="52f83-157">Choose **More options** `...` and then clear the checkmark next to **Group by folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="A opção Grupo por pasta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="52f83-159">A **opção Grupo por** pasta</span><span class="sxs-lookup"><span data-stu-id="52f83-159">The **Group by folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="52f83-160">Os recursos são organizados por tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="52f83-160">Resources are organized by file type.</span></span>  <span data-ttu-id="52f83-161">Em cada tipo de arquivo, os recursos são organizados em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="52f83-161">Within each file type, the resources are organized alphabetically.</span></span>  

    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="A guia Página após limpar a marca de seleção Grupo por pasta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="52f83-163">A **guia Página** após limpar a marca de seleção Grupo **por** pasta</span><span class="sxs-lookup"><span data-stu-id="52f83-163">The **Page** tab after clearing the **Group by folder** check mark</span></span>  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a><span data-ttu-id="52f83-164">Procurar por tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="52f83-164">Browse by file type</span></span>  

<span data-ttu-id="52f83-165">Para agrupar recursos com base no tipo de arquivo:</span><span class="sxs-lookup"><span data-stu-id="52f83-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="52f83-166">Escolha a **guia Aplicativo.**  A **ferramenta Application** é aberta.</span><span class="sxs-lookup"><span data-stu-id="52f83-166">Choose the **Application** tab.  The **Application** tool opens.</span></span>  <span data-ttu-id="52f83-167">Por padrão, **o** painel Manifesto geralmente é aberto primeiro.</span><span class="sxs-lookup"><span data-stu-id="52f83-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="A ferramenta Application" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="52f83-169">A **ferramenta Application**</span><span class="sxs-lookup"><span data-stu-id="52f83-169">The **Application** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52f83-170">Role para baixo até o painel **Quadros.**</span><span class="sxs-lookup"><span data-stu-id="52f83-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="O painel Quadros" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="52f83-172">O **painel Quadros**</span><span class="sxs-lookup"><span data-stu-id="52f83-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52f83-173">Expanda as seções nas quais você está interessado.</span><span class="sxs-lookup"><span data-stu-id="52f83-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="52f83-174">Escolha um recurso para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="52f83-174">Choose a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Exibir um recurso no painel Aplicativo" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="52f83-176">Exibir um recurso no painel **Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="52f83-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a><span data-ttu-id="52f83-177">Procurar arquivos por tipo no painel Rede</span><span class="sxs-lookup"><span data-stu-id="52f83-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="52f83-178">Navegue [até Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="52f83-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrar para CSS no Log de Rede" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="52f83-180">Filtrar para CSS no **Log de** Rede</span><span class="sxs-lookup"><span data-stu-id="52f83-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="52f83-181">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="52f83-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso - Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecionar os detalhes do recurso - Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Atividade de rede de log - Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: o elemento Frame em linha | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Saiba mais sobre desenvolvimento da Web | MDN"  

> [!NOTE]
> <span data-ttu-id="52f83-188">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52f83-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="52f83-189">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/resources/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="52f83-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="52f83-191">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52f83-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
