---
title: Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: cd6123f235af4ccb87338e1d4db12c03a93a9eaa
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684724"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="ce943-103">Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ce943-103">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>   



<span data-ttu-id="ce943-104">A ferramenta **problemas** no Microsoft Edge devtools reduz a notificação cansativo e resíduos do **console**.</span><span class="sxs-lookup"><span data-stu-id="ce943-104">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="ce943-105">Use-o para encontrar soluções para problemas detectados pelo navegador, como problemas com cookies e conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="ce943-105">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="ce943-106">No Microsoft Edge 84, a ferramenta **problemas** dá suporte a três tipos de problemas:</span><span class="sxs-lookup"><span data-stu-id="ce943-106">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="ce943-107">Problemas com cookies</span><span class="sxs-lookup"><span data-stu-id="ce943-107">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="ce943-108">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="ce943-108">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="ce943-109">Problemas com o COEP</span><span class="sxs-lookup"><span data-stu-id="ce943-109">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="ce943-110">O Microsoft Edge DevTools Team Plan para dar suporte a mais tipos de problemas em versões futuras do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ce943-110">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="ce943-111">Abrir a ferramenta problemas na gaveta do DevTools</span><span class="sxs-lookup"><span data-stu-id="ce943-111">Open the Issues tool in the DevTools drawer</span></span>   

1.  <span data-ttu-id="ce943-112">Acesse uma página, como [SameSite-sandbox.Glitch.me][GlitchSamesiteSandbox], que contém problemas para corrigir.</span><span class="sxs-lookup"><span data-stu-id="ce943-112">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="ce943-113">[Abra o devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="ce943-113">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="ce943-114">Selecione o botão **ir para problemas** na barra de aviso amarela.</span><span class="sxs-lookup"><span data-stu-id="ce943-114">Select the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="ce943-116">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="ce943-116">Figure 1.</span></span>  <span data-ttu-id="ce943-117">O botão **ir para problemas** na barra de aviso amarela quando problemas são detectados.</span><span class="sxs-lookup"><span data-stu-id="ce943-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="ce943-118">Ou, se preferir, selecione **problemas** no menu **mais ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="ce943-118">Alternatively, select **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Ferramenta problemas no menu mais ferramentas" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="ce943-120">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="ce943-120">Figure 2.</span></span>  <span data-ttu-id="ce943-121">Ferramenta **problemas** no menu **mais ferramentas**</span><span class="sxs-lookup"><span data-stu-id="ce943-121">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="ce943-122">Selecione o botão **recarregar página** , se necessário.</span><span class="sxs-lookup"><span data-stu-id="ce943-122">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Ferramenta problemas na gaveta DevTools com o botão recarregar página" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="ce943-124">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="ce943-124">Figure 3.</span></span>  <span data-ttu-id="ce943-125">Ferramenta **problemas** na gaveta devtools com o botão **recarregar página**</span><span class="sxs-lookup"><span data-stu-id="ce943-125">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="ce943-126">Os problemas relatados no **console** são muito difíceis de entender, como os avisos de cookies na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce943-126">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="ce943-127">Com base nos problemas relatados, talvez não seja claro o que você deve fazer.</span><span class="sxs-lookup"><span data-stu-id="ce943-127">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Ferramenta problemas na gaveta DevTools com três problemas de cookies" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="ce943-129">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="ce943-129">Figure 4.</span></span>  <span data-ttu-id="ce943-130">Ferramenta **problemas** na gaveta devtools com três problemas de cookies</span><span class="sxs-lookup"><span data-stu-id="ce943-130">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ce943-131">Exibir itens na ferramenta problemas</span><span class="sxs-lookup"><span data-stu-id="ce943-131">View items in the Issues tool</span></span>   

<span data-ttu-id="ce943-132">A ferramenta **problemas** na gaveta do devtools apresenta avisos em uma maneira estruturada, agregada e acionável.</span><span class="sxs-lookup"><span data-stu-id="ce943-132">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="ce943-133">Selecione um item na ferramenta **problemas** para obter orientação sobre como corrigir o problema e localizar os recursos afetados.</span><span class="sxs-lookup"><span data-stu-id="ce943-133">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marcar cookies entre sites como um problema seguro aberto na ferramenta problemas" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="ce943-135">Figura 5.</span><span class="sxs-lookup"><span data-stu-id="ce943-135">Figure 5.</span></span>  <span data-ttu-id="ce943-136">**Marcar cookies entre sites como** um problema seguro aberto na ferramenta **problemas**</span><span class="sxs-lookup"><span data-stu-id="ce943-136">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="ce943-137">Cada item tem quatro componentes:</span><span class="sxs-lookup"><span data-stu-id="ce943-137">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="ce943-138">Uma manchete descrevendo o problema.</span><span class="sxs-lookup"><span data-stu-id="ce943-138">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="ce943-139">Uma descrição que fornece o contexto e a solução.</span><span class="sxs-lookup"><span data-stu-id="ce943-139">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="ce943-140">Uma seção de **recursos afetados** que se vincula aos recursos dentro do contexto devtools apropriado, como o painel rede.</span><span class="sxs-lookup"><span data-stu-id="ce943-140">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="ce943-141">Links para outras diretrizes.</span><span class="sxs-lookup"><span data-stu-id="ce943-141">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="ce943-142">Selecione itens em **recursos afetados** para exibir detalhes.</span><span class="sxs-lookup"><span data-stu-id="ce943-142">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="ce943-143">No exemplo a seguir, a **marca cookies entre sites como** um problema seguro afeta um cookie e duas solicitações.</span><span class="sxs-lookup"><span data-stu-id="ce943-143">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Recursos afetados abertos na guia gaveta de problemas" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="ce943-145">Figura 6.</span><span class="sxs-lookup"><span data-stu-id="ce943-145">Figure 6.</span></span>  <span data-ttu-id="ce943-146">Recursos afetados abertos na ferramenta **problemas** na gaveta do devtools</span><span class="sxs-lookup"><span data-stu-id="ce943-146">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ce943-147">Exibir problemas no contexto</span><span class="sxs-lookup"><span data-stu-id="ce943-147">View issues in context</span></span>   

1.  <span data-ttu-id="ce943-148">Selecione um link de recurso para exibir o item no contexto apropriado no DevTools.</span><span class="sxs-lookup"><span data-stu-id="ce943-148">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="ce943-149">No exemplo a seguir, selecione `samesite-sandbox.glitch.me` em **solicitações** para mostrar os cookies anexados a essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="ce943-149">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Exibir o cookie afetado no painel de rede do DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="ce943-151">Figura 7.</span><span class="sxs-lookup"><span data-stu-id="ce943-151">Figure 7.</span></span>  <span data-ttu-id="ce943-152">Exibir o cookie afetado no painel de rede do DevTools</span><span class="sxs-lookup"><span data-stu-id="ce943-152">View the affected cookie in the DevTools Network panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="ce943-153">Role para ver o item com um problema: para o exemplo a seguir, o `ck02` Cookie.</span><span class="sxs-lookup"><span data-stu-id="ce943-153">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="ce943-154">Passe o mouse sobre a coluna **SameSite** para ver o `None` valor detectado pelo problema.</span><span class="sxs-lookup"><span data-stu-id="ce943-154">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Nenhum valor na coluna SameSite para o cookie ck02 no painel de rede do DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       <span data-ttu-id="ce943-156">Figura 8.</span><span class="sxs-lookup"><span data-stu-id="ce943-156">Figure 8.</span></span>  `None` <span data-ttu-id="ce943-157">valor na coluna **SameSite** para o `ck02` cookie no painel de **rede** devtools</span><span class="sxs-lookup"><span data-stu-id="ce943-157">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

<!--## Feedback  -->  



<!-- image links -->  

<!-- links -->  

[DevtoolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Testes de cookies SameSite | Problema"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Conteúdo misto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Política incorporada de origem cruzada | Grupo da Comunidade Incubator da Web"  

> [!NOTE]
> <span data-ttu-id="ce943-163">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="ce943-163">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ce943-164">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é criada por [Samuel Dutton][SamDutton] \ (defensora do desenvolvedor \).</span><span class="sxs-lookup"><span data-stu-id="ce943-164">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ce943-166">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ce943-166">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
