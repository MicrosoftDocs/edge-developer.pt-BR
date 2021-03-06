---
description: Use a ferramenta Problemas para encontrar e corrigir problemas com seu site.
title: Encontrar e corrigir problemas com a ferramenta Problemas do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e16bd926ea5bae35ad82f54ac5d1ae2028e3c59d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398970"
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

# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a><span data-ttu-id="6e7f4-104">Encontrar e corrigir problemas com a ferramenta Problemas do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6e7f4-104">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="6e7f4-105">A **ferramenta Problemas** no Microsoft Edge DevTools reduz a fatiga de notificação e a desordem do **Console**.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-105">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="6e7f4-106">Use-o para encontrar soluções para problemas detectados pelo navegador, como problemas de cookie e conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-106">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="6e7f4-107">No Microsoft Edge 84, a **ferramenta Issues** dá suporte a três tipos de problema:</span><span class="sxs-lookup"><span data-stu-id="6e7f4-107">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="6e7f4-108">Problemas de cookie</span><span class="sxs-lookup"><span data-stu-id="6e7f4-108">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="6e7f4-109">Conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="6e7f4-109">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="6e7f4-110">Problemas de COEP</span><span class="sxs-lookup"><span data-stu-id="6e7f4-110">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="6e7f4-111">A equipe do Microsoft Edge DevTools planeja dar suporte a mais tipos de problemas em versões futuras do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-111">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="6e7f4-112">Abra a ferramenta Problemas na gaveta DevTools</span><span class="sxs-lookup"><span data-stu-id="6e7f4-112">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="6e7f4-113">Navegue até uma página da Web, como [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], que contém problemas para corrigir.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-113">Navigate to a webpage, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="6e7f4-114">[Abra DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="6e7f4-114">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="6e7f4-115">Escolha o **botão Ir para Problemas** na barra de aviso amarelo.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-115">Choose the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Vá para o botão Problemas na barra de aviso amarelo quando Os problemas são detectados" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="6e7f4-117">O **botão Ir para Problemas** na barra de aviso amarelo quando Problemas são detectados.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="6e7f4-118">Como alternativa, escolha **Problemas** no menu **Mais ferramentas.**</span><span class="sxs-lookup"><span data-stu-id="6e7f4-118">Alternatively, choose **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Ferramenta Problemas no menu Mais ferramentas" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="6e7f4-120">**Ferramenta Problemas** no menu **Mais ferramentas**</span><span class="sxs-lookup"><span data-stu-id="6e7f4-120">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="6e7f4-121">Escolha o **botão Recarregar página,** se necessário.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-121">Choose the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Ferramenta Problemas no botão DevTools Drawer with Reload page" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="6e7f4-123">**Ferramenta Problemas** no botão DevTools Drawer with **Reload page**</span><span class="sxs-lookup"><span data-stu-id="6e7f4-123">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="6e7f4-124">Os problemas relatados no **Console** são difíceis de entender, como os avisos de cookie na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-124">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="6e7f4-125">Com base nos problemas relatados, pode não estar claro o que você deve fazer.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-125">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Ferramenta Problemas na Gaveta de DevTools com três problemas de cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="6e7f4-127">**Ferramenta Problemas** na Gaveta de DevTools com três problemas de cookie</span><span class="sxs-lookup"><span data-stu-id="6e7f4-127">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a><span data-ttu-id="6e7f4-128">Exibir itens na ferramenta Problemas</span><span class="sxs-lookup"><span data-stu-id="6e7f4-128">View items in the Issues tool</span></span>  

<span data-ttu-id="6e7f4-129">A **ferramenta Problemas** na Gaveta de DevTools apresenta avisos de forma estruturada, agregada e a ação.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-129">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="6e7f4-130">Escolha um item na ferramenta **Problemas** para obter orientações sobre como corrigir o problema e encontrar recursos afetados.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-130">Choose an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marcar cookies entre sites como problema seguro aberto na ferramenta Problemas" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="6e7f4-132">**Marcar cookies entre sites como problema** seguro aberto na ferramenta **Problemas**</span><span class="sxs-lookup"><span data-stu-id="6e7f4-132">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="6e7f4-133">Cada item tem quatro componentes:</span><span class="sxs-lookup"><span data-stu-id="6e7f4-133">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="6e7f4-134">Uma título que descreve o problema.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-134">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="6e7f4-135">Uma descrição que fornece o contexto e a solução.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-135">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="6e7f4-136">Uma **seção RECURSOS AFETADOs** que se vincula aos recursos no contexto apropriado do DevTools, como o painel Rede.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-136">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="6e7f4-137">Links para mais orientações.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-137">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="6e7f4-138">Escolha itens em **RECURSOS AFETADOs** para exibir detalhes.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-138">Choose items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="6e7f4-139">No exemplo a seguir, o **mark cross-site cookies as Secure** issue afeta um cookie e duas solicitações.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-139">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Recursos afetados abertos na ferramenta Problemas" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="6e7f4-141">Recursos afetados abertos na **ferramenta Problemas** na Gaveta de DevTools</span><span class="sxs-lookup"><span data-stu-id="6e7f4-141">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a><span data-ttu-id="6e7f4-142">Exibir problemas no contexto</span><span class="sxs-lookup"><span data-stu-id="6e7f4-142">View issues in context</span></span>  

1.  <span data-ttu-id="6e7f4-143">Escolha um link de recurso para exibir o item no contexto apropriado no DevTools.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-143">Choose a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="6e7f4-144">No exemplo a seguir, escolha `samesite-sandbox.glitch.me` em **Solicitações** para mostrar os cookies anexados a essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-144">In the following example, choose `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Exibir o cookie afetado na ferramenta Rede de DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="6e7f4-146">Exibir o cookie afetado na \*\*\*\* ferramenta Rede de DevTools</span><span class="sxs-lookup"><span data-stu-id="6e7f4-146">View the affected cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="6e7f4-147">Role para exibir o item com um problema: para o exemplo a seguir, o `ck02` cookie.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-147">Scroll to view the item with a problem:  for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="6e7f4-148">Passe o mouse na **coluna SameSite** para revisar `None` o valor detectado pelo problema.</span><span class="sxs-lookup"><span data-stu-id="6e7f4-148">Hover on the **SameSite** column to review the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Nenhum valor na coluna SameSite para o cookie ck02 na ferramenta Rede DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="6e7f4-150">na coluna **SameSite** para o `ck02` cookie na \*\*\*\* ferramenta Rede DevTools</span><span class="sxs-lookup"><span data-stu-id="6e7f4-150">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6e7f4-151">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6e7f4-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Testes de cookie sameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies sameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Conteúdo misto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Política de embedder entre origens | Grupo da Comunidade de Incubadores da Web"  

> [!NOTE]
> <span data-ttu-id="6e7f4-157">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6e7f4-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6e7f4-158">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é de autoria de [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="6e7f4-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6e7f4-160">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6e7f4-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
