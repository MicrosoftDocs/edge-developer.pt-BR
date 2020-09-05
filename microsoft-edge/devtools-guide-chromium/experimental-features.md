---
description: Os recursos experimentais mais recentes do Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, experimento
ms.openlocfilehash: a5793b6f4b67add313958ad4b8cee01cb7b09dbf
ms.sourcegitcommit: 7e3644e6b1d568ab795168e421c013814efa0073
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/04/2020
ms.locfileid: "10996156"
---
# <span data-ttu-id="c1a0b-104">Recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="c1a0b-104">Experimental features</span></span>  

<span data-ttu-id="c1a0b-105">Você pode usar os recursos experimentais que ainda estão em desenvolvimento no Microsoft Edge DevTools para testar e [fornecer comentários](#providing-feedback-on-experimental-features) antes que cada um seja liberado amplamente.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="c1a0b-106">Embora os recursos experimentais estejam disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o Microsoft Edge Canárias Channel.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="c1a0b-107">Ativar os recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="c1a0b-107">Turn on experimental features</span></span>  

<span data-ttu-id="c1a0b-108">Use as etapas a seguir para ativar \ (ou desligado \) recursos experimentais no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="c1a0b-109">[Abra o devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="c1a0b-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="c1a0b-110">Selecione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="c1a0b-110">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="c1a0b-111">Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="c1a0b-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="c1a0b-112">Abra o painel [configurações][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="c1a0b-113">Selecione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-113">Select `Shift`+`?`.</span></span>  <span data-ttu-id="c1a0b-114">Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="c1a0b-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="c1a0b-115">No lado esquerdo do painel **configurações** , selecione a seção **experimentos** .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="c1a0b-117">Lista de experimentos nas configurações do DevTools</span><span class="sxs-lookup"><span data-stu-id="c1a0b-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c1a0b-118">Na página **experimentos** , percorra a lista de todos os recursos experimentais disponíveis e marque a caixa de seleção ao lado de cada recurso que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="c1a0b-119">Feche e abra novamente o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="c1a0b-120">Os recursos experimentais são atualizados constantemente e podem causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="c1a0b-121">Para desativar um recurso experimental, abra a página **experimentos** e desmarque a caixa de seleção do recurso experimental que você deseja desativar.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="c1a0b-122">Recursos experimentais realçados</span><span class="sxs-lookup"><span data-stu-id="c1a0b-122">Highlighted experimental features</span></span>  

<span data-ttu-id="c1a0b-123">As seções a seguir descrevem os novos recursos experimentais que estão disponíveis no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="c1a0b-124">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="c1a0b-124">Experimental feature</span></span> | <span data-ttu-id="c1a0b-125">Microsoft Edge versão</span><span class="sxs-lookup"><span data-stu-id="c1a0b-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="c1a0b-126">Habilitar novos recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="c1a0b-126">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="c1a0b-127">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c1a0b-127">85 or later</span></span> |  
| [<span data-ttu-id="c1a0b-128">Habilitar o suporte para mover as guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="c1a0b-128">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="c1a0b-129">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c1a0b-129">85 or later</span></span> |  
| [<span data-ttu-id="c1a0b-130">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="c1a0b-130">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="c1a0b-131">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c1a0b-131">85 or later</span></span> |  
| [<span data-ttu-id="c1a0b-132">Habilitar console de rede</span><span class="sxs-lookup"><span data-stu-id="c1a0b-132">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="c1a0b-133">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c1a0b-133">85 or later</span></span> |  
| [<span data-ttu-id="c1a0b-134">Habilitar o Visualizador de ordem de origem</span><span class="sxs-lookup"><span data-stu-id="c1a0b-134">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="c1a0b-135">86 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c1a0b-135">86 or later</span></span> |  

### <span data-ttu-id="c1a0b-136">Habilitar novos recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="c1a0b-136">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="c1a0b-137">Aprimora as visualizações na página quando você depura sites que têm layouts de grade CSS.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-137">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="c1a0b-138">Você pode personalizar ainda mais as sobreposições nas configurações do DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-138">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Recurso de depuração de grade CSS" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="c1a0b-140">Recurso de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="c1a0b-140">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="c1a0b-141">Habilitar o suporte para mover as guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="c1a0b-141">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="c1a0b-142">Normalmente, ferramentas como **elementos** e **rede** só podem ser abertas no painel main \ (Top \) do devtools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-142">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="c1a0b-143">Da mesma forma, ferramentas como **modo de exibição 3D** e **problemas** só podem ser abertos no painel gaveta \ (inferior \) do devtools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-143">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="c1a0b-144">Ao escolher o experimento, você pode mover ferramentas entre os painéis superior e inferior passando o mouse sobre a guia, abrindo o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início** ou **mover para o fim**.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-144">When you choose the experiment, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="c1a0b-145">Este experimento permite que você personalize o layout do DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-145">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="c1a0b-146">Para mostrar ou ocultar o painel inferior, selecione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-146">To show or hide the bottom panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Mover guias entre painéis" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="c1a0b-148">Mover guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="c1a0b-148">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="c1a0b-149">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="c1a0b-149">Enable webhint</span></span>  

<span data-ttu-id="c1a0b-150">[webhint][WebhintMain] é uma ferramenta de código-fonte aberto que fornece comentários em tempo real sobre a acessibilidade, a compatibilidade entre navegadores, a segurança, o desempenho, a PWAs e outras questões de desenvolvimento da Web comuns dos sites.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-150">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="c1a0b-151">O experimento da [webhint][WebhintMain] traz o comentário webhint para devtools no painel [problemas][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-151">The [webhint][WebhintMain] experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="c1a0b-152">Você pode selecionar o problema para ver a documentação sobre como corrigir o problema e uma lista dos recursos afetados em seu site.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-152">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="c1a0b-153">Selecione um link de recurso para abrir o painel de **rede**, **fontes**ou **elementos** relevantes no devtools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-153">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Comentários da webhint no painel problemas" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="c1a0b-155">Comentários da webhint no painel **problemas**</span><span class="sxs-lookup"><span data-stu-id="c1a0b-155">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="c1a0b-156">Habilitar console de rede</span><span class="sxs-lookup"><span data-stu-id="c1a0b-156">Enable Network Console</span></span>  

<span data-ttu-id="c1a0b-157">**Console de rede** é o título de trabalho de um experimento para fazer solicitações de rede sintéticas por http.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-157">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="c1a0b-158">Você pode usar o experimento do **console de rede** para enviar solicitações de API da Web.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-158">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="c1a0b-159">Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-159">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="c1a0b-160">Para usar o console de rede:</span><span class="sxs-lookup"><span data-stu-id="c1a0b-160">To use the Network Console:</span></span>  

1.  <span data-ttu-id="c1a0b-161">Abra o painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-161">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="c1a0b-162">Localize a solicitação de rede que você deseja alterar e envie novamente.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-162">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="c1a0b-163">Abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **Editar e reproduzir**.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-163">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="c1a0b-164">Quando o **console de rede** for aberto, edite as informações de solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-164">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="c1a0b-165">Selecione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-165">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.png" alt-text="Console de rede na gaveta do console" lightbox="./media/network-network-console.png":::
   <span data-ttu-id="c1a0b-167">**Console de rede** na gaveta do **console**</span><span class="sxs-lookup"><span data-stu-id="c1a0b-167">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### <span data-ttu-id="c1a0b-168">Habilitar o Visualizador de ordem de origem</span><span class="sxs-lookup"><span data-stu-id="c1a0b-168">Enable Source Order Viewer</span></span>  

<span data-ttu-id="c1a0b-169">O **Visualizador de ordem de origem** é o título de trabalho de um experimento para exibir a ordem dos elementos na fonte da página.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-169">**Source Order Viewer** is the working title of an experiment to display the order of elements in the page source.</span></span>  <span data-ttu-id="c1a0b-170">Você pode usar o **Visualizador de ordem de origem** experimento para encontrar problemas de acessibilidade em suas páginas, pois a ordem de exibição na tela pode ser diferente da ordem da fonte, que confundi os usuários do leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-170">You may use the **Source Order Viewer** experiment to find accessibility issues in your pages since the display order on-screen may differ from the order of the source, which confuses screen reader users.</span></span>  

<span data-ttu-id="c1a0b-171">Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-171">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="c1a0b-172">Para usar o Visualizador de ordem de origem:</span><span class="sxs-lookup"><span data-stu-id="c1a0b-172">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="c1a0b-173">Abrir o painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-173">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="c1a0b-174">Abra o painel **acessibilidade** no painel gaveta \ (inferior \).</span><span class="sxs-lookup"><span data-stu-id="c1a0b-174">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="c1a0b-175">Na seção **Visualizador de ordem de origem** , marque a caixa de seleção **Mostrar ordem de origem** .</span><span class="sxs-lookup"><span data-stu-id="c1a0b-175">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="c1a0b-176">Realce qualquer elemento HTML para exibir uma sobreposição que a ordem na fonte da página.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-176">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visualizador de ordem de origem no painel Acessibilidade" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="c1a0b-178">**Visualizador de ordem de origem** no painel **acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="c1a0b-178">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="c1a0b-179">Recursos experimentais anteriores</span><span class="sxs-lookup"><span data-stu-id="c1a0b-179">Previous experimental features</span></span>  

*   <span data-ttu-id="c1a0b-180">o [modo de exibição 3D][Devtools3dViewIndex] agora está disponível e ativado por padrão no Microsoft Edge versão 83 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-180">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="c1a0b-181">[Personalizar atalhos de teclado][DevtoolsCustomKeyboardShortcuts] agora está disponível e ativado por padrão no Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-181">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>
## <span data-ttu-id="c1a0b-182">Fornecer comentários sobre os recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="c1a0b-182">Providing feedback on experimental features</span></span>  

<span data-ttu-id="c1a0b-183">Para fornecer comentários sobre o Microsoft Edge DevTools experimentos ou qualquer outro item relacionado ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1a0b-183">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="c1a0b-184">Envie seus comentários usando o ícone **enviar comentários** no devtools</span><span class="sxs-lookup"><span data-stu-id="c1a0b-184">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="c1a0b-185">Tweet em [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="c1a0b-185">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>   

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="O ícone enviar comentários no Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="c1a0b-187">O ícone **enviar comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="c1a0b-187">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Modo de exibição 3D | Documentos da Microsoft"  
[DevtoolsIssues]: ./issues/index.md "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsOpen]: ./open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Personalizar atalhos de teclado no Microsoft Edge DevTools | Documentos da Microsoft"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint" 
