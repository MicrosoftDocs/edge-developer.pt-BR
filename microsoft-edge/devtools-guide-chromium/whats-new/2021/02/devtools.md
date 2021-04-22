---
description: Suporte de depuração para CSS Flexbox, tela de alerta de desempenho na página da Web, atualizações de ferramenta de problemas e muito mais
title: O que há de novo no DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: 3653bd2293f96a6ddfb84d8e1c7492bea78c15c1
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514400"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-90"></a><span data-ttu-id="a4b34-104">O que há de novo no DevTools (Microsoft Edge 90)</span><span class="sxs-lookup"><span data-stu-id="a4b34-104">What's New In DevTools (Microsoft Edge 90)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a><span data-ttu-id="a4b34-105">Ferramentas de grupo juntas no Modo de Foco</span><span class="sxs-lookup"><span data-stu-id="a4b34-105">Group tools together in Focus Mode</span></span>  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

<span data-ttu-id="a4b34-106">O Modo de Foco é uma interface experimental que permite agrupar diferentes ferramentas com base em seus próprios cenários de depuração.</span><span class="sxs-lookup"><span data-stu-id="a4b34-106">Focus Mode is an experimental interface that allows you to group different tools together based on your own debugging scenarios.</span></span>  <span data-ttu-id="a4b34-107">A nova **Barra de Atividades** exibida à esquerda inclui grupos de ferramentas predefinidos, como **Layout** e **Depuração**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-107">The new **Activity Bar** displayed on the left includes predefined tool groups such as **Layout** and **Debugging**.</span></span>  <span data-ttu-id="a4b34-108">Para personalizar cada grupo de ferramentas, feche as ferramentas com o ícone **Fechar** \(`X`\) ou adicione novas ferramentas com o ícone **Mais ferramentas** \(`+`\).</span><span class="sxs-lookup"><span data-stu-id="a4b34-108">To customize each tool group, close tools with the **Close** \(`X`\) icon or add new tools with the **More tools** \(`+`\) icon.</span></span>  

<span data-ttu-id="a4b34-109">Para ativar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] e escolha as caixas de seleção ao lado de **Modo de foco e Dicas de ferramentas do DevTools** e **Habilitar os menus da guia do botão + para abrir mais ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-109">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="a4b34-110">Para obter mais informações sobre este recurso ou para comentar com perguntas e ideias, navegue até [DevTools: Interface do usuário Modo de Foco][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="a4b34-110">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Exibir a Barra de Atividades" lightbox="../../media/2021/02/focus-mode.msft.png":::
   <span data-ttu-id="a4b34-112">Exibir a **Barra de Atividades**</span><span class="sxs-lookup"><span data-stu-id="a4b34-112">Display the **Activity Bar**</span></span>  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="a4b34-113">Saiba mais sobre o DevTools com dicas de ferramentas informativas</span><span class="sxs-lookup"><span data-stu-id="a4b34-113">Learn about DevTools with informative tooltips</span></span>  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

<span data-ttu-id="a4b34-114">O recurso de Dicas de Ferramentas do DevTools ajuda você a aprender sobre todas as diferentes ferramentas e painéis.</span><span class="sxs-lookup"><span data-stu-id="a4b34-114">The DevTools Tooltips feature helps you learn about all the different tools and panes.</span></span>  <span data-ttu-id="a4b34-115">Escolha o ícone Ajuda \(`?`\) na parte inferior da **Barra de Atividades** para alternar as dicas de ferramentas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4b34-115">Choose the Help \(`?`\) icon at the bottom of the **Activity Bar** to toggle tooltips in the DevTools.</span></span>  <span data-ttu-id="a4b34-116">Quando as dicas de ferramentas estiverem habilitadas, passe o mouse sobre cada região delineada do DevTools para saber mais sobre como usar a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a4b34-116">When tooltips are on, hover over each outlined region of DevTools to learn more about how to use the tool.</span></span>  <span data-ttu-id="a4b34-117">Para ativar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] e escolha as caixas de seleção ao lado de **Modo de foco e Dicas de ferramentas do DevTools** e **Habilitar os menus da guia do botão + para abrir mais ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-117">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="a4b34-118">Para obter mais informações sobre este recurso ou para comentar com perguntas e ideias, navegue até [DevTools: Interface do usuário Modo de Foco][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="a4b34-118">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Escolha o ícone de Ajuda (?) Na Barra de Atividades para exibir as dicas de ferramentas" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   <span data-ttu-id="a4b34-120">Escolha o ícone Ajuda \(`?`\) na **Barra de Atividades** para exibir dicas de ferramenta</span><span class="sxs-lookup"><span data-stu-id="a4b34-120">Choose the Help \(`?`\) icon in the **Activity Bar** to display tooltips</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="a4b34-121">Personalize os atalhos do teclado em Configurações</span><span class="sxs-lookup"><span data-stu-id="a4b34-121">Customize keyboard shortcuts in Settings</span></span>  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

<span data-ttu-id="a4b34-122">Agora você pode personalizar o atalho de teclado para qualquer ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4b34-122">You may now customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="a4b34-123">Para editar um atalho de teclado, execute as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="a4b34-123">To edit a keyboard shortcut, complete the following actions.</span></span>  

1.  <span data-ttu-id="a4b34-124">Abra o DevTools e escolha **Atalhos** > **de Configurações**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-124">Open the DevTools, and then choose **Settings** > **Shortcuts**.</span></span>  
1.  <span data-ttu-id="a4b34-125">Escolha a ação que você deseja personalizar.</span><span class="sxs-lookup"><span data-stu-id="a4b34-125">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="a4b34-126">Escolha Editar \(</span><span class="sxs-lookup"><span data-stu-id="a4b34-126">Choose the Edit \(</span></span>![Editar o ícone de Atalho de Teclado](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)<span data-ttu-id="a4b34-128">\) ícone.</span><span class="sxs-lookup"><span data-stu-id="a4b34-128">\) icon.</span></span>  
1.  <span data-ttu-id="a4b34-129">Selecione as teclas que você deseja vincular à ação.</span><span class="sxs-lookup"><span data-stu-id="a4b34-129">Select the keys you want to bind to the action.</span></span>  
1.  <span data-ttu-id="a4b34-130">Escolha a marca de seleção \(</span><span class="sxs-lookup"><span data-stu-id="a4b34-130">Choose the checkmark \(</span></span>![Ícone de Atalho de Teclado marca de seleção](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="a4b34-132">\) ícone.</span><span class="sxs-lookup"><span data-stu-id="a4b34-132">\) icon.</span></span>  
    
<span data-ttu-id="a4b34-133">Para obter mais informações sobre como personalizar e editar atalhos, navegue até [Personalizar atalhos de teclado no Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="a4b34-133">For more information about customizing and editing shortcuts, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="a4b34-134">Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="a4b34-134">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personalize os atalhos de teclado nas Configurações do DevTools em Atalhos com um atalho no modo de edição" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   <span data-ttu-id="a4b34-136">Personalize os atalhos de teclado nas [Configurações do DevTools][DevtoolsCustomizeIndexSettings] em Atalhos com um atalho no modo de edição</span><span class="sxs-lookup"><span data-stu-id="a4b34-136">Customize keyboard shortcuts in the [DevTools Settings][DevtoolsCustomizeIndexSettings] on Shortcuts with a shortcut in edit mode</span></span>  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a><span data-ttu-id="a4b34-137">Atualização 1.1.4 da extensão do Microsoft Edge DevTools para o Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a4b34-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span></span>  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

<span data-ttu-id="a4b34-138">O [Microsoft Edge Developer Tools para o Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extensão 1.1.4 para o Microsoft Visual Studio Code agora exibe um favicon próximo a cada uma das instâncias do DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4b34-138">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code now displays a favicon next to each of the DevTools instances.</span></span>  <span data-ttu-id="a4b34-139">As mensagens do console do Microsoft Edge agora são exibidas no **Console do DevTools** em **Saída** do Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="a4b34-139">Console messages from Microsoft Edge now display in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  <span data-ttu-id="a4b34-140">O Microsoft Visual Studio Code atualiza as extensões automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a4b34-140">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="a4b34-141">Para atualizar manualmente para a versão 1.1.4, navegue até [Atualizar uma extensão manualmente][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span><span class="sxs-lookup"><span data-stu-id="a4b34-141">To manually update to version 1.1.4, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="a4b34-142">Você pode registrar problemas e contribuir para a extensão no repositório do GitHub [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="a4b34-142">You may file issues and contribute to the extension on the [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub repo.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a4b34-143">A figura a seguir exibe as mensagens de uma página da Web de exemplo registrada na ferramenta **Console** no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4b34-143">The following figure displays messages from an example webpage logged in the **Console** tool in Microsoft Edge.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a4b34-144">A figura a seguir exibe as mesmas mensagens da página da Web de exemplo registrada no **Console do DevTools** em **Saída** do Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="a4b34-144">The following figure displays the same messages from the example webpage logged in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Exibir uma mensagem no Console do Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         <span data-ttu-id="a4b34-146">Exibir uma mensagem no Console do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a4b34-146">Display a message in Console in Microsoft Edge DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Exibir a mesma mensagem no Console do DevTools em Saída do Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         <span data-ttu-id="a4b34-148">Exibir a mesma mensagem no Console do DevTools em Saída do Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a4b34-148">Display the same message in the DevTools Console under Output of Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a><span data-ttu-id="a4b34-149">Edição com CSS flexbox aprimorada com editor visual flexbox e múltiplas sobreposições</span><span class="sxs-lookup"><span data-stu-id="a4b34-149">Improved CSS flexbox editing with visual flexbox editor and multiple overlays</span></span>  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

<span data-ttu-id="a4b34-150">O DevTools agora possui ferramentas de depuração do CSS flexbox dedicadas.</span><span class="sxs-lookup"><span data-stu-id="a4b34-150">DevTools now has dedicated CSS flexbox debugging tools.</span></span>  <span data-ttu-id="a4b34-151">Se o `display: flex` ou `display: inline-flex` estilo CSS for aplicado a um elemento HTML, um `flex` ícone será exibido próximo a esse elemento na ferramenta **Elementos**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-151">If the `display: flex` or `display: inline-flex` CSS style is applied to an HTML element, a `flex` icon displays next to that element in the **Elements** tool.</span></span>  <span data-ttu-id="a4b34-152">Para exibir \(ou ocultar\) uma sobreposição flexível na página da Web, escolha o ícone`flex`.</span><span class="sxs-lookup"><span data-stu-id="a4b34-152">To display \(or hide\) a flex overlay on the webpage, choose the `flex` icon.</span></span>  <span data-ttu-id="a4b34-153">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [1166710][CR1166710] e [1175699][CR1175699].</span><span class="sxs-lookup"><span data-stu-id="a4b34-153">To review the history of this feature in the Chromium open-source project, navigate to Issues [1166710][CR1166710] and [1175699][CR1175699].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a4b34-154">Para abrir o editor do**Flexbox**, navegue até o painel **Estilos** e escolha o novo ícone ao lado do `display: flex` ou `display: inline-flex` estilo.</span><span class="sxs-lookup"><span data-stu-id="a4b34-154">To open the **Flexbox** editor, navigate to the **Styles** pane and choose the new icon next to the `display: flex` or `display: inline-flex` style.</span></span>  <span data-ttu-id="a4b34-155">O editor do **Flexbox** fornece uma maneira rápida de editar as propriedades do flexbox.</span><span class="sxs-lookup"><span data-stu-id="a4b34-155">The **Flexbox** editor provides a quick way to edit the flexbox properties.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a4b34-156">Além disso, a seção do **Flexbox** no painel **Layout** exibe todos os elementos do flexbox na página da Web.</span><span class="sxs-lookup"><span data-stu-id="a4b34-156">In addition, the **Flexbox** section in the **Layout** pane displays all of the flexbox elements on the webpage.</span></span>  <span data-ttu-id="a4b34-157">Você pode alternar a sobreposição de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="a4b34-157">You may toggle the overlay of each element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Ferramentas de depuração do CSS flexbox" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         <span data-ttu-id="a4b34-159">Ferramentas de depuração do CSS flexbox</span><span class="sxs-lookup"><span data-stu-id="a4b34-159">CSS flexbox debugging tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Seção do Flexbox no painel Layout" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         <span data-ttu-id="a4b34-161">Seção do **Flexbox** no painel **Layout**</span><span class="sxs-lookup"><span data-stu-id="a4b34-161">**Flexbox** section in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a><span data-ttu-id="a4b34-162">Melhorias na navegação do teclado para solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="a4b34-162">Keyboard navigation improvements for network requests</span></span>  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

<span data-ttu-id="a4b34-163">Anteriormente, você não conseguia expandir ou recolher a cadeia de solicitações usando as teclas de direção do teclado no painel **Iniciador**, ao contrário do DOM na ferramenta **Elementos**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-163">Previously, you were not able to expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane, unlike the DOM in the **Elements** tool.</span></span>  <span data-ttu-id="a4b34-164">Quando uma solicitação de rede é selecionada na ferramenta **Rede**, o painel **Iniciador** exibe a cadeia de solicitações que iniciou a solicitação atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="a4b34-164">When a network request is selected in the **Network** tool, the **Initiator** pane displays the chain of requests that initiated the currently selected request.</span></span>  

<span data-ttu-id="a4b34-165">No Microsoft Edge versão 90, você pode expandir ou recolher a cadeia de solicitações usando as teclas de direção no teclado no painel **Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-165">In Microsoft Edge version 90, you may expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane.</span></span>  <span data-ttu-id="a4b34-166">A solicitação de rede focada na rede também está agora em destaque.</span><span class="sxs-lookup"><span data-stu-id="a4b34-166">The focused network request in the chain is also now highlighted.</span></span>  <span data-ttu-id="a4b34-167">Para saber mais sobre os iniciadores na ferramenta **Rede**, navegue até [Exibir iniciadores e dependências][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="a4b34-167">To learn more about initiators in the **Network** tool, navigate to [Display initiators and dependencies][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span></span>  <span data-ttu-id="a4b34-168">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [1158276][CR1158276] e [1160637][CR1160637].</span><span class="sxs-lookup"><span data-stu-id="a4b34-168">To review the history of this feature in the Chromium open-source project, navigate to Issues [1158276][CR1158276] and [1160637][CR1160637].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Escolha uma solicitação de Rede e escolha o painel Iniciador" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         <span data-ttu-id="a4b34-170">Escolha uma solicitação de Rede e escolha o painel **Iniciador**</span><span class="sxs-lookup"><span data-stu-id="a4b34-170">Choose a Network request and choose the **Initiator** pane</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Expanda ou recolha a solicitação de cadeia de iniciador e siga a linha destacada" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         <span data-ttu-id="a4b34-172">Expanda ou recolha a solicitação de cadeia de iniciador e siga a linha destacada</span><span class="sxs-lookup"><span data-stu-id="a4b34-172">Expand or collapse the request initiator chain and follow the highlighted row</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a><span data-ttu-id="a4b34-173">A filtragem no Console é mais consistente</span><span class="sxs-lookup"><span data-stu-id="a4b34-173">Filtering in the Console is more consistent</span></span>  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

<span data-ttu-id="a4b34-174">Enquanto você filtra com a [Barra Lateral do Console][DevtoolsConsoleReferenceOpenConsoleSidebar], os filtros na lista suspensa [Níveis de Registro][DevtoolsConsoleReferenceFilterByLogLevel] não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a4b34-174">While you filter with the [Console Sidebar][DevtoolsConsoleReferenceOpenConsoleSidebar], the filters in the [Log Levels][DevtoolsConsoleReferenceFilterByLogLevel] dropdown are not available.</span></span>  <span data-ttu-id="a4b34-175">Anteriormente, a lista suspensa **Níveis de Registro** era destacada quando você passava o mouse sobre ela, mesmo quando um filtro da **Barra Lateral do Console** era escolhido.</span><span class="sxs-lookup"><span data-stu-id="a4b34-175">Previously, the **Log Levels** dropdown highlighted when you hovered on it, even while a filter from the **Console Sidebar** was chosen.</span></span>  <span data-ttu-id="a4b34-176">No Microsoft Edge versão 90, a lista suspensa **Níveis de Registro** não é mais realçada quando você passa o mouse sobre ela enquanto um filtro da **Barra Lateral do Console** é escolhido.</span><span class="sxs-lookup"><span data-stu-id="a4b34-176">In Microsoft Edge version 90, the **Log Levels** dropdown no longer highlights when you hover on it while a filter from the **Console Sidebar** is chosen.</span></span>  <span data-ttu-id="a4b34-177">Para saber mais sobre a filtragem no **Console**, navegue até [Filtrar Mensagens][DevtoolsConsoleReferenceFilterMessages].</span><span class="sxs-lookup"><span data-stu-id="a4b34-177">To learn more about filtering in the **Console**, navigate to [Filter Messages][DevtoolsConsoleReferenceFilterMessages].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Anteriormente, se você abrisse a barra lateral do Console e passasse o mouse sobre os níveis Padrão, ele ficava realçado" lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         <span data-ttu-id="a4b34-179">Anteriormente, se você abrisse a **barra lateral do Console** e passasse o mouse sobre os **níveis Padrão**, ele ficava realçado</span><span class="sxs-lookup"><span data-stu-id="a4b34-179">Previously, if you open the **Console sidebar** and hover on **Default levels** it was highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="A partir do Microsoft Edge 90, se você escolhesse a barra lateral do Console e passasse o mouse sobre os níveis padrão, ele não será realçada" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         <span data-ttu-id="a4b34-181">A partir do Microsoft Edge 90, se você escolhesse a **barra lateral do Console** e passasse o mouse sobre os **níveis padrão**, ele não será realçada</span><span class="sxs-lookup"><span data-stu-id="a4b34-181">Starting in Microsoft Edge 90, if you choose the **Console sidebar** and hover on **Default levels**, it does not highlight</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="a4b34-182">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="a4b34-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a><span data-ttu-id="a4b34-183">O console agora escapa de caracteres de aspas duplas</span><span class="sxs-lookup"><span data-stu-id="a4b34-183">The Console now escapes double quote characters</span></span>  

<span data-ttu-id="a4b34-184">Anteriormente, o **Console** não produzia caracteres de aspas duplas \(`"`\) válidos em strings do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a4b34-184">Previously, the **Console** did not output valid double quote \(`"`\) characters in JavaScript strings.</span></span>  <span data-ttu-id="a4b34-185">A partir do Microsoft Edge versão 90, o **Console** gera strings do JavaScript usando caracteres de aspas duplas escapadas \ (`"`\).</span><span class="sxs-lookup"><span data-stu-id="a4b34-185">Starting in Microsoft Edge version 90, the **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters.</span></span>  <span data-ttu-id="a4b34-186">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1178530][CR1178530].</span><span class="sxs-lookup"><span data-stu-id="a4b34-186">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178530][CR1178530].</span></span>  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="O Console gera strings do JavaScript usando caracteres de aspas duplas escapadas (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   <span data-ttu-id="a4b34-188">O **Console** gera strings do JavaScript usando caracteres de aspas duplas escapadas \(`"`\)</span><span class="sxs-lookup"><span data-stu-id="a4b34-188">The **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters</span></span>  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a><span data-ttu-id="a4b34-189">Emular a gama de cores do recurso de mídia do CSS</span><span class="sxs-lookup"><span data-stu-id="a4b34-189">Emulate the CSS color-gamut media feature</span></span>  

<span data-ttu-id="a4b34-190">A consulta de mídia de [gama de cores][ChromestatusFeature5354410980933632] emula a faixa aproximada de cores suportada pelo navegador e o dispositivo que você está testando.</span><span class="sxs-lookup"><span data-stu-id="a4b34-190">The [color-gamut][ChromestatusFeature5354410980933632] media query emulates the approximate range of colors supported by the browser and the device you are testing.</span></span>  <span data-ttu-id="a4b34-191">A lista suspensa em **Emular a gama de cores do recurso de mídia do CSS** contém espaços de cores que o DevTools pode emular.</span><span class="sxs-lookup"><span data-stu-id="a4b34-191">The dropdown under **Emulate CSS media feature color-gamut** contains color spaces that DevTools may emulate.</span></span>  <span data-ttu-id="a4b34-192">Por exemplo, para acionar uma `color-gamut: p3` consulta de mídia, escolha **gama de cores: p3** no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="a4b34-192">For example, to trigger a `color-gamut: p3` media query, choose **color-gamut: p3** from the dropdown.</span></span>  

<span data-ttu-id="a4b34-193">Para emular a gama de cores do recurso de mídia do CSS, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="a4b34-193">To emulate the CSS color-gamut media feature, complete the following actions.</span></span>  

1.  <span data-ttu-id="a4b34-194">Abra o [Menu de Comando][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="a4b34-194">Open the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
1.  <span data-ttu-id="a4b34-195">Digite `Rendering`.</span><span class="sxs-lookup"><span data-stu-id="a4b34-195">Type `Rendering`.</span></span>  
1.  <span data-ttu-id="a4b34-196">Execute o comando **Mostrar Renderização**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-196">Run the **Show Rendering** command.</span></span>  
1.  <span data-ttu-id="a4b34-197">Navegue até **Emular a gama de cores do recurso de mídia do CSS** e escolha uma opção.</span><span class="sxs-lookup"><span data-stu-id="a4b34-197">Navigate to **Emulate CSS media feature color-gamut** and choose an option.</span></span>  

<span data-ttu-id="a4b34-198">Para saber mais sobre o recurso `color-gamut`, navegue até [Qualidade de Exibição de Cores: O recurso de 'gama de cores'][CsswgDraftsMediaqueries4ColorGamut].</span><span class="sxs-lookup"><span data-stu-id="a4b34-198">To learn more about the `color-gamut` feature, navigate to [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span></span>  <span data-ttu-id="a4b34-199">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1073887][CR1073887].</span><span class="sxs-lookup"><span data-stu-id="a4b34-199">To review the history of this feature in the Chromium open-source project, navigate to Issue [1073887][CR1073887].</span></span>  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emular a gama de cores do recurso de mídia do CSS" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   <span data-ttu-id="a4b34-201">Emular a gama de cores do recurso de mídia do CSS</span><span class="sxs-lookup"><span data-stu-id="a4b34-201">Emulate the CSS color-gamut media feature</span></span>  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a><span data-ttu-id="a4b34-202">Ferramentas de Aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="a4b34-202">Improved Progressive Web Apps tooling</span></span>  

#### <a name="pwa-installability-warning-in-the-console"></a><span data-ttu-id="a4b34-203">Aviso de instalabilidade do PWA no Console</span><span class="sxs-lookup"><span data-stu-id="a4b34-203">PWA installability warning in the Console</span></span>  

<span data-ttu-id="a4b34-204">O **Console** agora exibe uma mensagem de aviso de instalação dos [Aplicativos Web Progressivos (PWA)][ProgressiveWebAppsIndex] mais detalhada com um link para [Aprimoramento da detecção de suporte offline do Aplicativo Web Progressivo][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span><span class="sxs-lookup"><span data-stu-id="a4b34-204">The **Console** now displays a more detailed [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] installability warning message with a link to [Improving Progressive Web App offline support detection][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span></span>  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Aviso de instalabilidade do PWA na ferramenta Console" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   <span data-ttu-id="a4b34-206">Aviso de instalabilidade do PWA na ferramenta **Console**</span><span class="sxs-lookup"><span data-stu-id="a4b34-206">PWA installability warning in **Console** tool</span></span>  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a><span data-ttu-id="a4b34-207">Aviso de comprimento da descrição do PWA no painel Manifesto</span><span class="sxs-lookup"><span data-stu-id="a4b34-207">PWA description length warning in the Manifest pane</span></span>

<span data-ttu-id="a4b34-208">O painel **Manifesto** agora exibe uma mensagem de aviso se a descrição do manifesto exceder 324 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a4b34-208">The **Manifest** pane now displays a warning message if the manifest description exceeds 324 characters.</span></span>  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Aviso de truncamento da descrição do PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   <span data-ttu-id="a4b34-210">Aviso de truncamento da descrição do PWA</span><span class="sxs-lookup"><span data-stu-id="a4b34-210">PWA description truncate warning</span></span>  
:::image-end:::  

<span data-ttu-id="a4b34-211">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [965802][CR965802], [1146450][CR1146450] e [1169689][CR1169689].</span><span class="sxs-lookup"><span data-stu-id="a4b34-211">To review the history of this feature in the Chromium open-source project, navigate to Issues [965802][CR965802], [1146450][CR1146450], and [1169689][CR1169689].</span></span>  

### <a name="new-remote-address-space-column-in-the-network-tool"></a><span data-ttu-id="a4b34-212">Nova coluna Espaço de Endereço Remoto na ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="a4b34-212">New Remote Address Space column in the Network tool</span></span>  

<!-- does not work in canary 90.0.813.0 -->  
<span data-ttu-id="a4b34-213">A nova coluna **Espaço de Endereço Remoto** exibe o espaço de endereço do IP da rede de cada recurso da rede.</span><span class="sxs-lookup"><span data-stu-id="a4b34-213">The new **Remote Address Space** column displays the network IP address space of each network resource.</span></span>  <span data-ttu-id="a4b34-214">Para exibir a nova coluna Espaço de Endereço Remoto, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="a4b34-214">To display the new Remote Address Space column, complete the following actions.</span></span>  

1.  <span data-ttu-id="a4b34-215">Navegue até a ferramenta **Rede**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-215">Navigate to the **Network** tool.</span></span>  
1.  <span data-ttu-id="a4b34-216">Na tabela Solicitações, passe o mouse sobre a linha do cabeçalho e abra o menu contextual \(clique com o botão direito\).</span><span class="sxs-lookup"><span data-stu-id="a4b34-216">In the Requests table, hover on the header row, and open the contextual menu \(right-click\).</span></span>  <span data-ttu-id="a4b34-217">Para saber como adicionar ou remover colunas da tabela Solicitações, navegue até [Adicionar ou remover colunas][DevtoolsNetworkReferenceAddRemoveColumns].</span><span class="sxs-lookup"><span data-stu-id="a4b34-217">To learn how to add or remove columns from the Requests table, navigate to [Add or remove columns][DevtoolsNetworkReferenceAddRemoveColumns].</span></span>  
1.  <span data-ttu-id="a4b34-218">Escolha **Espaço de Endereço Remoto**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-218">Choose **Remote Address Space**.</span></span>  
    
<span data-ttu-id="a4b34-219">A tabela Solicitações agora exibe uma nova coluna com o cabeçalho denominado**Espaço de Endereço Remoto**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-219">The Requests table now displays a new column with the header named **Remote Address Space**.</span></span>  <span data-ttu-id="a4b34-220">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1128885][CR1128885].</span><span class="sxs-lookup"><span data-stu-id="a4b34-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1128885][CR1128885].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="No menu contextual, escolha Espaço de Endereço Remoto" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         <span data-ttu-id="a4b34-222">No menu contextual, escolha o **Espaço de Endereço Remoto**</span><span class="sxs-lookup"><span data-stu-id="a4b34-222">In the contextual menu, choose the **Remote Address Space**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="A tabela Solicitações agora exibe a coluna Espaço de Endereço Remoto" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         <span data-ttu-id="a4b34-224">A tabela Solicitações agora exibe a coluna **Espaço de Endereço Remoto**</span><span class="sxs-lookup"><span data-stu-id="a4b34-224">The Requests table now displays the **Remote Address Space** column</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a><span data-ttu-id="a4b34-225">Exibir recursos permitidos e não permitidos na visualização de detalhes do Quadro</span><span class="sxs-lookup"><span data-stu-id="a4b34-225">Display allowed and disallowed features in the Frame details view</span></span>  

<span data-ttu-id="a4b34-226">A exibição de detalhes do Quadro agora exibe uma lista de recursos permitidos e não permitidos do navegador controlados pela [Política de Permissões][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span><span class="sxs-lookup"><span data-stu-id="a4b34-226">The Frame details view now displays a list of allowed and disallowed browser features controlled by the [Permissions Policy][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span></span>  <span data-ttu-id="a4b34-227">A Política de Permissões é uma API de plataforma Web que permite \(ou bloqueia\) o uso de recursos do navegador de uma página da Web em um quadro individual ou em iframes que ela incorpora.</span><span class="sxs-lookup"><span data-stu-id="a4b34-227">Permissions Policy is a web platform API that allows \(or blocks\) a webpage the use of browser features in an individual frame or in iframes that it embeds.</span></span>  <span data-ttu-id="a4b34-228">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="a4b34-228">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Recursos permitidos e não permitidos com base na Política de Permissão" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   <span data-ttu-id="a4b34-230">Recursos permitidos e não permitidos com base na Política de Permissão</span><span class="sxs-lookup"><span data-stu-id="a4b34-230">Allowed and disallowed features based on the Permission Policy</span></span>  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a><span data-ttu-id="a4b34-231">Nova coluna SameParty no painel Cookies</span><span class="sxs-lookup"><span data-stu-id="a4b34-231">New SameParty column in the Cookies pane</span></span>  

<span data-ttu-id="a4b34-232">O painel **Cookies** na ferramenta **Aplicativo** agora exibe o atributo `SameParty` para cada cookie.</span><span class="sxs-lookup"><span data-stu-id="a4b34-232">The **Cookies** pane in the **Application** tool now displays the `SameParty` attribute for each cookie.</span></span>  <span data-ttu-id="a4b34-233">O atributo `SameParty` é um novo atributo booleano para indicar se um cookie está incluído em solicitações para origens dos mesmos [Conjuntos de Primeira Parte][GithubPrivacycgFirstPartySets].</span><span class="sxs-lookup"><span data-stu-id="a4b34-233">The `SameParty` attribute is a new boolean attribute to indicate whether a cookie is included in requests to origins of the same [First-Party Sets][GithubPrivacycgFirstPartySets].</span></span>  <span data-ttu-id="a4b34-234">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1161427][CR1161427].</span><span class="sxs-lookup"><span data-stu-id="a4b34-234">To review the history of this feature in the Chromium open-source project, navigate to Issue [1161427][CR1161427].</span></span>  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Coluna SameParty no painel Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   <span data-ttu-id="a4b34-236">Coluna **SameParty** no painel **Cookies**</span><span class="sxs-lookup"><span data-stu-id="a4b34-236">**SameParty** column in the **Cookies** pane</span></span>  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a><span data-ttu-id="a4b34-237">A propriedade fn.displayName na ferramenta Console agora está obsoleta</span><span class="sxs-lookup"><span data-stu-id="a4b34-237">fn.displayName property in the Console tool is now deprecated</span></span>  

<span data-ttu-id="a4b34-238">Anteriormente, a `fn.displayName` propriedade permitia controlar os nomes de depuração das funções a serem exibidas em `error.stack`e nos rastreamentos de pilha do DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4b34-238">Previously, the `fn.displayName` property allowed you to control debug names for functions to display in `error.stack` and in DevTools stack traces.</span></span>  <span data-ttu-id="a4b34-239">A partir do Microsoft Edge versão 90, a propriedade `fn.displayName` foi descontinuada e substituída pela propriedade `fn.name`.</span><span class="sxs-lookup"><span data-stu-id="a4b34-239">Starting in Microsoft Edge version 90, the `fn.displayName` property is now deprecated, and replaced by the `fn.name` property.</span></span>  <span data-ttu-id="a4b34-240">Use o método padrão `Object.defineProperty` para definir a propriedade `fn.name`.</span><span class="sxs-lookup"><span data-stu-id="a4b34-240">Use the standard `Object.defineProperty` method to define the `fn.name` property.</span></span>  <span data-ttu-id="a4b34-241">Para saber mais sobre `fn.name`, navegue até [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span><span class="sxs-lookup"><span data-stu-id="a4b34-241">To learn more about `fn.name`, navigate to [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span></span>  <span data-ttu-id="a4b34-242">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1177685][CR1177685].</span><span class="sxs-lookup"><span data-stu-id="a4b34-242">To review the history of this feature in the Chromium open-source project, navigate to Issue [1177685][CR1177685].</span></span>  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Um exemplo da propriedade fn.name para controlar os nomes de depuração para funções" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   <span data-ttu-id="a4b34-244">Um exemplo da propriedade `fn.name` para controlar os nomes de depuração para funções</span><span class="sxs-lookup"><span data-stu-id="a4b34-244">An example of the `fn.name` property to control debug names for functions</span></span>  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a><span data-ttu-id="a4b34-245">Exibição em árvore de acessibilidade completa na ferramenta Elementos</span><span class="sxs-lookup"><span data-stu-id="a4b34-245">Full accessibility tree view in the Elements tool</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="a4b34-246">Este experimento fornece uma **exibição em árvore de acessibilidade completa** na ferramenta **Elementos**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-246">This experiment provides a **full accessibility tree view** in the **Elements** tool.</span></span>  <span data-ttu-id="a4b34-247">O painel [Acessibilidade][DevtoolsAccessibilityReferenceTheAccessibilityPane] fornece uma visualização em árvore de acessibilidade parcial que exibe a cadeia ancestral direta do nó raiz ao nó inspecionado.</span><span class="sxs-lookup"><span data-stu-id="a4b34-247">The [Accessibility][DevtoolsAccessibilityReferenceTheAccessibilityPane] pane provides a partial accessibility tree view, that displays the direct ancestor chain from the root node to the inspected node.</span></span>  
<span data-ttu-id="a4b34-248">Depois de ativar esse experimento e recarregar o DevTools, escolha um dos seguintes botões para alternar a exibição na ferramenta Elementos para todos os elementos na página da Web.</span><span class="sxs-lookup"><span data-stu-id="a4b34-248">After you turn on this experiment and reload the DevTools, choose one of the following buttons to switch the display in the Elements tool for all elements on the webpage.</span></span>  

*   <span data-ttu-id="a4b34-249">Para exibir em árvore de acessibilidade completa, escolha **Alternar para o modo de exibição em Árvore de Acessibilidade**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-249">To display the full accessibility tree view , choose the **Switch to Accessibility Tree view**.</span></span>  
*   <span data-ttu-id="a4b34-250">Para exibir a exibição da árvore DOM, escolha **Alternar para exibição da árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-250">To display the DOM tree view, choose the **Switch to DOM Tree view**.</span></span>  
    
<span data-ttu-id="a4b34-251">Para ativar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Ativar visualização em árvore de acessibilidade completa no painel Elementos**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-251">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkbox next to **Enable full accessibility tree view in Elements pane**.</span></span>  <span data-ttu-id="a4b34-252">Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [887173][CR887173].</span><span class="sxs-lookup"><span data-stu-id="a4b34-252">To review the history of this feature in the Chromium open-source project, navigate to Issue [887173][CR887173].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Exibir o modo de exibição árvore DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         <span data-ttu-id="a4b34-254">Exibir o **modo de exibição DOM**</span><span class="sxs-lookup"><span data-stu-id="a4b34-254">Display the **DOM view**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Exibir o modo de exibição em árvore de acessibilidade completa" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         <span data-ttu-id="a4b34-256">Exibir o modo de exibição em **Árvore de Acessibilidade Completa**</span><span class="sxs-lookup"><span data-stu-id="a4b34-256">Display the **Full Accessibility Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="a4b34-257">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4b34-257">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="a4b34-258">Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="a4b34-258">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="a4b34-259">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4b34-259">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="a4b34-260">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a4b34-260">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "O painel de Acessibilidade - referência de acessibilidade | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nível de registro - referência do console | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filtrar mensagens - Referência do Console | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Abra a Barra Lateral do Console - referência do Console | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalize os atalhos do teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Ative os menus da guia do botão + para abrir mais ferramentas - Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Adicionar ou remover colunas - Referência de Análise de Rede | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Exibir iniciadores e dependências - Referência de Análise de Rede | Microsoft Docs"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Visão geral progressiva dos Aplicativos Web no Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace da Extensão | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Melhorar a detecção de suporte offline do Aplicativo Web Progressivo | Desenvolvedores do Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "consulta de mídia de gama de cores | Status da Plataforma Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir a personalização de atalhos de teclado/associações de chave | Bugs do Chromium"  
[CR887173]: https://crbug.com/887173 "Problema 887173: DevTools: Inspeção da Árvore de Acessibilidade Completa | Bugs do Chromium"  
[CR965802]: https://crbug.com/965802 "Problema 965802: Implementar a detecção de recursos offline mais precisa do trabalho de serviço | Bugs do Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problema 1073887: DevTools: @media (Gama de cores: ...) emulação de espaço de cores | Bugs do Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problema 1128885: Suporte do DevTools para CORS-RFC1918 | Bugs do Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problema 1146450: [Android] Implementar instalações de folha inferior | Bugs do Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problema 1158276: Não é possível expandir/contrair o painel 'Solicitação de cadeia de iniciador' usando as teclas de direção na seção 'Rede' do DevTools | Bugs do Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Política de Permissões] Implementar suporte do devtool para políticas de permissões | Bugs do Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problema 1160637: O Foco em 'Solicitação de cadeia de iniciador' é visto incompleto na seção 'Rede' da janela 'Dev Tools' | Bugs de cromo"  
[CR1161427]: https://crbug.com/1161427 "Problema 1161427: &#9730; suporte à depuração de atributo de cookie SameParty no DevTools | Bugs do Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problema 1166710: Ativar o experimento de ferramentas do flexbox por padrão | Bugs do Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problema 1169689: A folha inferior de instalação do PWA não deve apresentar categorias | Bugs do Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problema 1175699: Editor do Flexbox | Bugs do Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problema 1177685: Remover o suporte não-padronizado fn.displayName | Bugs do Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problema 1178530: O console não evita aspas duplas ao imprimir as cadeias de caracteres | Bugs do Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Qualidade de Exibição de Cores: O recurso de 'gama de cores' | Rascunhos do Editor do Grupo de Trabalho do CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Interface do Usuário do Modo de Foco - MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Conjuntos de Primeira Parte | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicação da Política de Permissões | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> <span data-ttu-id="a4b34-300">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a4b34-300">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a4b34-301">A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-90) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="a4b34-301">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-90) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a4b34-303">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a4b34-303">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
