---
title: Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d837723ed68c6d088e7b345ae86c7a0312b46496
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986126"
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

# <span data-ttu-id="d676f-103">Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d676f-103">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="d676f-104">A ferramenta **problemas** no Microsoft Edge devtools reduz a notificação cansativo e resíduos do **console**.</span><span class="sxs-lookup"><span data-stu-id="d676f-104">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="d676f-105">Use-o para encontrar soluções para problemas detectados pelo navegador, como problemas com cookies e conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="d676f-105">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="d676f-106">No Microsoft Edge 84, a ferramenta **problemas** dá suporte a três tipos de problemas:</span><span class="sxs-lookup"><span data-stu-id="d676f-106">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="d676f-107">Problemas com cookies</span><span class="sxs-lookup"><span data-stu-id="d676f-107">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="d676f-108">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="d676f-108">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="d676f-109">Problemas com o COEP</span><span class="sxs-lookup"><span data-stu-id="d676f-109">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="d676f-110">O Microsoft Edge DevTools Team Plan para dar suporte a mais tipos de problemas em versões futuras do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d676f-110">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="d676f-111">Abrir a ferramenta problemas na gaveta do DevTools</span><span class="sxs-lookup"><span data-stu-id="d676f-111">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="d676f-112">Acesse uma página, como [SameSite-sandbox.Glitch.me][GlitchSamesiteSandbox], que contém problemas para corrigir.</span><span class="sxs-lookup"><span data-stu-id="d676f-112">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="d676f-113">[Abra o devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="d676f-113">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="d676f-114">Selecione o botão **ir para problemas** na barra de aviso amarela.</span><span class="sxs-lookup"><span data-stu-id="d676f-114">Select the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="d676f-116">O botão **ir para problemas** na barra de aviso amarela quando problemas são detectados.</span><span class="sxs-lookup"><span data-stu-id="d676f-116">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="d676f-117">Ou, se preferir, selecione **problemas** no menu **mais ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="d676f-117">Alternatively, select **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Ferramenta problemas no menu mais ferramentas" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="d676f-119">Ferramenta **problemas** no menu **mais ferramentas**</span><span class="sxs-lookup"><span data-stu-id="d676f-119">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="d676f-120">Selecione o botão **recarregar página** , se necessário.</span><span class="sxs-lookup"><span data-stu-id="d676f-120">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Ferramenta problemas na gaveta DevTools com o botão recarregar página" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="d676f-122">Ferramenta **problemas** na gaveta devtools com o botão **recarregar página**</span><span class="sxs-lookup"><span data-stu-id="d676f-122">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="d676f-123">Os problemas relatados no **console** são muito difíceis de entender, como os avisos de cookies na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="d676f-123">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="d676f-124">Com base nos problemas relatados, talvez não seja claro o que você deve fazer.</span><span class="sxs-lookup"><span data-stu-id="d676f-124">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Ferramenta problemas na gaveta DevTools com três problemas de cookies" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="d676f-126">Ferramenta **problemas** na gaveta devtools com três problemas de cookies</span><span class="sxs-lookup"><span data-stu-id="d676f-126">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d676f-127">Exibir itens na ferramenta problemas</span><span class="sxs-lookup"><span data-stu-id="d676f-127">View items in the Issues tool</span></span>  

<span data-ttu-id="d676f-128">A ferramenta **problemas** na gaveta do devtools apresenta avisos em uma maneira estruturada, agregada e acionável.</span><span class="sxs-lookup"><span data-stu-id="d676f-128">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="d676f-129">Selecione um item na ferramenta **problemas** para obter orientação sobre como corrigir o problema e localizar os recursos afetados.</span><span class="sxs-lookup"><span data-stu-id="d676f-129">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marcar cookies entre sites como um problema seguro aberto na ferramenta problemas" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="d676f-131">**Marcar cookies entre sites como** um problema seguro aberto na ferramenta **problemas**</span><span class="sxs-lookup"><span data-stu-id="d676f-131">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="d676f-132">Cada item tem quatro componentes:</span><span class="sxs-lookup"><span data-stu-id="d676f-132">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="d676f-133">Uma manchete descrevendo o problema.</span><span class="sxs-lookup"><span data-stu-id="d676f-133">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="d676f-134">Uma descrição que fornece o contexto e a solução.</span><span class="sxs-lookup"><span data-stu-id="d676f-134">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="d676f-135">Uma seção de **recursos afetados** que se vincula aos recursos dentro do contexto devtools apropriado, como o painel rede.</span><span class="sxs-lookup"><span data-stu-id="d676f-135">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="d676f-136">Links para outras diretrizes.</span><span class="sxs-lookup"><span data-stu-id="d676f-136">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="d676f-137">Selecione itens em **recursos afetados** para exibir detalhes.</span><span class="sxs-lookup"><span data-stu-id="d676f-137">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="d676f-138">No exemplo a seguir, a **marca cookies entre sites como** um problema seguro afeta um cookie e duas solicitações.</span><span class="sxs-lookup"><span data-stu-id="d676f-138">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Recursos afetados abertos na guia gaveta de problemas" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="d676f-140">Recursos afetados abertos na ferramenta **problemas** na gaveta do devtools</span><span class="sxs-lookup"><span data-stu-id="d676f-140">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d676f-141">Exibir problemas no contexto</span><span class="sxs-lookup"><span data-stu-id="d676f-141">View issues in context</span></span>  

1.  <span data-ttu-id="d676f-142">Selecione um link de recurso para exibir o item no contexto apropriado no DevTools.</span><span class="sxs-lookup"><span data-stu-id="d676f-142">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="d676f-143">No exemplo a seguir, selecione `samesite-sandbox.glitch.me` em **solicitações** para mostrar os cookies anexados a essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="d676f-143">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Exibir o cookie afetado no painel de rede do DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="d676f-145">Exibir o cookie afetado no painel de **rede** do devtools</span><span class="sxs-lookup"><span data-stu-id="d676f-145">View the affected cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="d676f-146">Role para ver o item com um problema: para o exemplo a seguir, o `ck02` Cookie.</span><span class="sxs-lookup"><span data-stu-id="d676f-146">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="d676f-147">Passe o mouse sobre a coluna **SameSite** para ver o `None` valor detectado pelo problema.</span><span class="sxs-lookup"><span data-stu-id="d676f-147">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Nenhum valor na coluna SameSite para o cookie ck02 no painel de rede do DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="d676f-149">valor na coluna **SameSite** para o `ck02` cookie no painel de **rede** devtools</span><span class="sxs-lookup"><span data-stu-id="d676f-149">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

## <span data-ttu-id="d676f-150">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d676f-150">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Testes de cookies SameSite | Problema"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Conteúdo misto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Política incorporada de origem cruzada | Grupo da Comunidade Incubator da Web"  

> [!NOTE]
> <span data-ttu-id="d676f-156">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="d676f-156">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d676f-157">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é criada por [Samuel Dutton][SamDutton] \ (defensora do desenvolvedor \).</span><span class="sxs-lookup"><span data-stu-id="d676f-157">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d676f-159">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d676f-159">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
