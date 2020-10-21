---
description: Use a ferramenta problemas para localizar e corrigir problemas com o website.
title: Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4691db9542ecff93d1b59e243844109e0c730d23
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124723"
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

# <span data-ttu-id="4c5a3-104">Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4c5a3-104">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="4c5a3-105">A ferramenta **problemas** no Microsoft Edge devtools reduz a notificação cansativo e resíduos do **console**.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-105">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="4c5a3-106">Use-o para encontrar soluções para problemas detectados pelo navegador, como problemas com cookies e conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-106">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="4c5a3-107">No Microsoft Edge 84, a ferramenta **problemas** dá suporte a três tipos de problemas:</span><span class="sxs-lookup"><span data-stu-id="4c5a3-107">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="4c5a3-108">Problemas com cookies</span><span class="sxs-lookup"><span data-stu-id="4c5a3-108">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="4c5a3-109">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="4c5a3-109">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="4c5a3-110">Problemas com o COEP</span><span class="sxs-lookup"><span data-stu-id="4c5a3-110">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="4c5a3-111">O Microsoft Edge DevTools Team Plan para dar suporte a mais tipos de problemas em versões futuras do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-111">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="4c5a3-112">Abrir a ferramenta problemas na gaveta do DevTools</span><span class="sxs-lookup"><span data-stu-id="4c5a3-112">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="4c5a3-113">Acesse uma página, como [SameSite-sandbox.Glitch.me][GlitchSamesiteSandbox], que contém problemas para corrigir.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-113">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="4c5a3-114">[Abra o devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="4c5a3-114">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="4c5a3-115">Selecione o botão **ir para problemas** na barra de aviso amarela.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-115">Select the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="4c5a3-117">O botão **ir para problemas** na barra de aviso amarela quando problemas são detectados.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="4c5a3-118">Ou, se preferir, escolha **problemas** no menu **mais ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="4c5a3-118">Alternatively, choose **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="4c5a3-120">Ferramenta **problemas** no menu **mais ferramentas**</span><span class="sxs-lookup"><span data-stu-id="4c5a3-120">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="4c5a3-121">Selecione o botão **recarregar página** , se necessário.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-121">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="4c5a3-123">Ferramenta **problemas** na gaveta devtools com o botão **recarregar página**</span><span class="sxs-lookup"><span data-stu-id="4c5a3-123">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="4c5a3-124">Os problemas relatados no **console** são muito difíceis de entender, como os avisos de cookies na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-124">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="4c5a3-125">Com base nos problemas relatados, talvez não seja claro o que você deve fazer.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-125">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="4c5a3-127">Ferramenta **problemas** na gaveta devtools com três problemas de cookies</span><span class="sxs-lookup"><span data-stu-id="4c5a3-127">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4c5a3-128">Exibir itens na ferramenta problemas</span><span class="sxs-lookup"><span data-stu-id="4c5a3-128">View items in the Issues tool</span></span>  

<span data-ttu-id="4c5a3-129">A ferramenta **problemas** na gaveta do devtools apresenta avisos em uma maneira estruturada, agregada e acionável.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-129">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="4c5a3-130">Selecione um item na ferramenta **problemas** para obter orientação sobre como corrigir o problema e localizar os recursos afetados.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-130">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="4c5a3-132">**Marcar cookies entre sites como** um problema seguro aberto na ferramenta **problemas**</span><span class="sxs-lookup"><span data-stu-id="4c5a3-132">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="4c5a3-133">Cada item tem quatro componentes:</span><span class="sxs-lookup"><span data-stu-id="4c5a3-133">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="4c5a3-134">Uma manchete descrevendo o problema.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-134">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="4c5a3-135">Uma descrição que fornece o contexto e a solução.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-135">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="4c5a3-136">Uma seção de **recursos afetados** que se vincula aos recursos dentro do contexto devtools apropriado, como o painel rede.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-136">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="4c5a3-137">Links para outras diretrizes.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-137">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="4c5a3-138">Selecione itens em **recursos afetados** para exibir detalhes.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-138">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="4c5a3-139">No exemplo a seguir, a **marca cookies entre sites como** um problema seguro afeta um cookie e duas solicitações.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-139">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="4c5a3-141">Recursos afetados abertos na ferramenta **problemas** na gaveta do devtools</span><span class="sxs-lookup"><span data-stu-id="4c5a3-141">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4c5a3-142">Exibir problemas no contexto</span><span class="sxs-lookup"><span data-stu-id="4c5a3-142">View issues in context</span></span>  

1.  <span data-ttu-id="4c5a3-143">Selecione um link de recurso para exibir o item no contexto apropriado no DevTools.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-143">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="4c5a3-144">No exemplo a seguir, selecione `samesite-sandbox.glitch.me` em **solicitações** para mostrar os cookies anexados a essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-144">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="4c5a3-146">Exibir o cookie afetado no painel de **rede** do devtools</span><span class="sxs-lookup"><span data-stu-id="4c5a3-146">View the affected cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="4c5a3-147">Role para ver o item com um problema: para o exemplo a seguir, o `ck02` Cookie.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-147">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="4c5a3-148">Passe o mouse sobre a coluna **SameSite** para ver o `None` valor detectado pelo problema.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-148">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="4c5a3-150">valor na coluna **SameSite** para o `ck02` cookie no painel de **rede** devtools</span><span class="sxs-lookup"><span data-stu-id="4c5a3-150">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

## <span data-ttu-id="4c5a3-151">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4c5a3-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Testes de cookies SameSite | Problema"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Conteúdo misto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Política incorporada de origem cruzada | Grupo da Comunidade Incubator da Web"  

> [!NOTE]
> <span data-ttu-id="4c5a3-157">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="4c5a3-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4c5a3-158">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é criada por [Samuel Dutton][SamDutton] \ (defensora do desenvolvedor \).</span><span class="sxs-lookup"><span data-stu-id="4c5a3-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4c5a3-160">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4c5a3-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
