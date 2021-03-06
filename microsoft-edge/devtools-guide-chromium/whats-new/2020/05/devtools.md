---
description: Use o DevTools no modo de alto contraste do Windows, match keyboard shortcuts in the DevTools to Visual Studio Code e muito mais.
title: Novidades no DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 701c328c1dc975a81129049fe2931139757205c3
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398571"
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

# <a name="whats-new-in-devtools-microsoft-edge-84"></a><span data-ttu-id="4294f-104">Novidades no DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="4294f-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4294f-105">Comunicados da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4294f-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="4294f-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="4294f-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="4294f-107">Confira os comunicados para experimentar novos recursos no DevTools, no Microsoft Visual Studio Code e muito mais.</span><span class="sxs-lookup"><span data-stu-id="4294f-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="4294f-108">Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="4294f-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a><span data-ttu-id="4294f-109">Usar o DevTools no modo de alto contraste do Windows</span><span class="sxs-lookup"><span data-stu-id="4294f-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="4294f-110">O Microsoft Edge DevTools agora é exibido no modo de alto contraste quando o Windows está no modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="4294f-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="O Microsoft Edge DevTools no modo de alto contraste" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="4294f-112">O Microsoft Edge DevTools no modo de alto contraste</span><span class="sxs-lookup"><span data-stu-id="4294f-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-113">[Siga as instruções para ativar o modo de alto contraste no Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="4294f-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="4294f-114">Para abrir o DevTools no Microsoft Edge, selecione `F12` ou `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="4294f-114">To open the DevTools in Microsoft Edge, select `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="4294f-115">Os DevTools são exibidos no modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="4294f-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="4294f-116">O Microsoft Edge DevTools atualmente suporta o modo de alto contraste no Windows, mas não no macOS.</span><span class="sxs-lookup"><span data-stu-id="4294f-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span>  

<span data-ttu-id="4294f-117">Problema do Chromium [#1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="4294f-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a><span data-ttu-id="4294f-118">Corresponder atalhos de teclado no DevTools para Visual Studio Código</span><span class="sxs-lookup"><span data-stu-id="4294f-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="4294f-119">Com seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team) e o rastreador de problemas públicos [do Chromium,][CRIssuesList]a equipe do Microsoft Edge DevTools aprendeu que você queria a capacidade de personalizar atalhos de teclado no DevTools.</span><span class="sxs-lookup"><span data-stu-id="4294f-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="4294f-120">No Microsoft Edge 84, agora você pode corresponder atalhos de teclado no DevTools a [Visual Studio Code,][VisualStudioCode]que é apenas um dos recursos em que a equipe está trabalhando para personalização de atalho.</span><span class="sxs-lookup"><span data-stu-id="4294f-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VisualStudioCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Corresponder atalhos de teclado no DevTools para Visual Studio Código" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="4294f-122">O Microsoft Edge DevTools no modo de alto contraste</span><span class="sxs-lookup"><span data-stu-id="4294f-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-123">Para experimentar o experimento, abra Configurações do DevTools selecionando ou escolhendo o ícone de configurações de DevTools no canto superior direito do `?` ![ ][ImageSettingsIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="4294f-123">To try the experiment, open DevTools Settings by selecting `?` or choosing the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="4294f-124">Navegue até **a seção Experimentos** e verifique **Habilitar configurações de atalhos de teclado personalizadas (requer recarga)**.</span><span class="sxs-lookup"><span data-stu-id="4294f-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="4294f-125">Agora, recarregue o DevTools, abra Configurações novamente e navegue até a **seção Atalhos.**</span><span class="sxs-lookup"><span data-stu-id="4294f-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="4294f-126">Escolha **DevTools (Padrão)** no menu suspenso Corresponder **atalhos** e selecione **Visual Studio Código**.</span><span class="sxs-lookup"><span data-stu-id="4294f-126">Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="4294f-127">Os atalhos de teclado no DevTools agora corresponderão aos atalhos para ações equivalentes no Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="4294f-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="4294f-128">Por exemplo, o atalho do teclado para pausar ou continuar executando um script no [Visual Studio Code][VisualStudioCodeShortcuts] é `F5` .</span><span class="sxs-lookup"><span data-stu-id="4294f-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="4294f-129">Com a **predefinição DevTools (Padrão),** esse mesmo atalho no DevTools é, mas com Visual Studio código predefinido, esse atalho agora `F8` também é \*\*\*\* `F5` .</span><span class="sxs-lookup"><span data-stu-id="4294f-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="4294f-130">O recurso está disponível no Microsoft Edge 84 como um experimento, portanto, compartilhe seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team) com a equipe!</span><span class="sxs-lookup"><span data-stu-id="4294f-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="4294f-131">Problema do Chromium [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="4294f-131">Chromium issue [#174309][CR174309]</span></span>  

### <a name="remote-debug-surface-duo-emulators"></a><span data-ttu-id="4294f-132">Emuladores do Surface Duo de depuração remota</span><span class="sxs-lookup"><span data-stu-id="4294f-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="4294f-133">Agora você pode depurar remotamente o conteúdo da Web em execução no [emulador do Surface Duo][DualScreensAndroidEmulator] usando a potência total do [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="4294f-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="4294f-134">Com o [emulador do Surface Duo,][DualScreensAndroidEmulator]você pode testar como o conteúdo da Web é renderizável em uma nova classe de dispositivos de tela dupla e dobrável.</span><span class="sxs-lookup"><span data-stu-id="4294f-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="4294f-135">O emulador executa o sistema operacional Android e fornece o [aplicativo Android do Microsoft Edge.][AndroidEdge]</span><span class="sxs-lookup"><span data-stu-id="4294f-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="4294f-136">Carregue o conteúdo da Web no [aplicativo do Microsoft Edge][AndroidEdge] e depure-o com o Microsoft Edge [DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="4294f-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="O aplicativo do Microsoft Edge em execução no emulador do Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="4294f-138">O aplicativo Microsoft Edge no emulador do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4294f-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-139">A página em uma instância da área de trabalho do Microsoft Edge mostra o `edge://inspect` **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][PwaIndex] que estão sendo executados no [emulador do Surface Duo.][DualScreensAndroidEmulator] [][DesktopEdge]</span><span class="sxs-lookup"><span data-stu-id="4294f-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="A edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="4294f-141">A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador</span><span class="sxs-lookup"><span data-stu-id="4294f-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="4294f-142">Escolha **inspecionar** a guia ou o PWA que você deseja depurar para abrir o [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="4294f-142">Choose **inspect** for the tab or PWA that you want to debug to open the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="4294f-143">Siga o guia passo a passo para depurar remotamente o conteúdo [da Web no emulador do Surface Duo.][DevToolsRemoteDebugDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="4294f-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <a name="resize-the-devtools-drawer-more-easily"></a><span data-ttu-id="4294f-144">Resize a gaveta DevTools com mais facilidade</span><span class="sxs-lookup"><span data-stu-id="4294f-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="4294f-145">No Microsoft Edge 83 ou anterior, você só foi capaz de resizer a [Gaveta de DevTools][DevToolsDrawer] pairando na barra de ferramentas da Gaveta.</span><span class="sxs-lookup"><span data-stu-id="4294f-145">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the toolbar of the Drawer.</span></span>  <span data-ttu-id="4294f-146">A Gaveta se comportava de forma diferente dos outros controles de ressarção para painéis no DevTools, onde você passar o mouse na borda do painel para ressilá-lo.</span><span class="sxs-lookup"><span data-stu-id="4294f-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane to resize it.</span></span>  <span data-ttu-id="4294f-147">Escolha a imagem a seguir para exibir como ressizing the Drawer funcionou na versão 83 ou anterior do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4294f-147">Choose the following image to display how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="4294f-149">Resizing the DevTools Drawer in Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="4294f-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="4294f-150">A partir do Microsoft Edge 84, você agora é capaz de ressarcionar a Gaveta pairando sobre a borda da Gaveta.</span><span class="sxs-lookup"><span data-stu-id="4294f-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="4294f-151">Essa alteração alinha o comportamento resizing the DevTools Drawer com a maneira como você resize outros painéis no DevTools.</span><span class="sxs-lookup"><span data-stu-id="4294f-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="4294f-152">Escolha a imagem a seguir para exibir o resizing em ação no Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="4294f-152">Choose the following image to display resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="4294f-154">Resizing the DevTools Drawer in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="4294f-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="4294f-155">Problema do Chromium [#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="4294f-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <a name="screencasting-navigation-buttons-display-focus"></a><span data-ttu-id="4294f-156">Botões de navegação de screencasting exibem o foco</span><span class="sxs-lookup"><span data-stu-id="4294f-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="4294f-157">Ao depurar remotamente um dispositivo [Android,][DevToolsRemoteDebugAndroid]um [dispositivo Windows 10][DevToolsRemoteDebugWindows]ou [um emulador do Surface Duo,][DevToolsRemoteDebugDuoEmulator]você pode alternar a telacasting com o ícone Deggle Screencast no canto superior esquerdo do ![ ][ImageScreencastingIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="4294f-157">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="4294f-158">Com a screencasting habilitada, você pode navegar na guia no Microsoft Edge no dispositivo remoto da janela DevTools.</span><span class="sxs-lookup"><span data-stu-id="4294f-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="4294f-159">No Microsoft Edge 84, esses botões de navegação agora também estão acessíveis ao teclado.</span><span class="sxs-lookup"><span data-stu-id="4294f-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Selecione Shift+Tab na barra de URL em tela mostra o foco no botão Atualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="4294f-161">Selecionar na barra de URL em `Shift` + `Tab` tela mostra o foco no **botão Atualizar**</span><span class="sxs-lookup"><span data-stu-id="4294f-161">Select `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="4294f-162">Problema do Chromium [#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="4294f-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <a name="network-panel-details-pane-is-now-accessible"></a><span data-ttu-id="4294f-163">Painel Detalhes do painel de rede agora está acessível</span><span class="sxs-lookup"><span data-stu-id="4294f-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="4294f-164">No Microsoft Edge 84, o [painel Detalhes][DevToolsNetworkDetails] na ferramenta **Rede** agora tem foco ao abri-lo para um recurso no Log [de Rede.][DevToolsNetworkLog]</span><span class="sxs-lookup"><span data-stu-id="4294f-164">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** tool now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="4294f-165">Essa alteração permite que os leitores de tela leiam e interajam com o conteúdo do painel **Detalhes.**</span><span class="sxs-lookup"><span data-stu-id="4294f-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="O painel Detalhes no painel Rede tem foco quando aberto" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="4294f-167">O **painel Detalhes** na ferramenta **Rede** tem foco quando aberto</span><span class="sxs-lookup"><span data-stu-id="4294f-167">The **Details** pane in the **Network** tool takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="4294f-168">Problema do Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="4294f-168">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="4294f-169">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="4294f-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="4294f-170">As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 84 que contribuíram para o projeto Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="4294f-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="4294f-171">Corrigir problemas de site com a nova ferramenta Problemas na Gaveta de DevTools</span><span class="sxs-lookup"><span data-stu-id="4294f-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="4294f-172">A nova **ferramenta Issues** na DevTools Drawer foi criada para ajudar a reduzir a fatiga de notificação e a desordem do **Console.**</span><span class="sxs-lookup"><span data-stu-id="4294f-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="4294f-173">Atualmente, o **Console** é o local central para desenvolvedores de site, bibliotecas, estruturas e Microsoft Edge registrar mensagens, avisos e erros.</span><span class="sxs-lookup"><span data-stu-id="4294f-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="4294f-174">A **ferramenta Issues** agrega avisos do navegador de forma estruturada, agregada e a ação, links para recursos afetados no Microsoft Edge DevTools e fornece orientações sobre como corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="4294f-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="4294f-175">Com o tempo, mais e mais avisos são a tona no Microsoft Edge na ferramenta **Problemas,** em vez do **Console,** o que deve ajudar a reduzir a desordem no **Console**.</span><span class="sxs-lookup"><span data-stu-id="4294f-175">Over time, more and more warnings are surfaced in Microsoft Edge in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="4294f-176">Para começar, navegue até [Encontrar e corrigir problemas com a ferramenta Problemas do Microsoft Edge DevTools.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="4294f-176">To get started, navigate to [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="A ferramenta Problemas na Gaveta de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="4294f-178">A **ferramenta Problemas** na Gaveta de DevTools</span><span class="sxs-lookup"><span data-stu-id="4294f-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-179">Problema do Chromium [#1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="4294f-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a><span data-ttu-id="4294f-180">Exibir informações de acessibilidade na dica de ferramenta Inspecionar Modo</span><span class="sxs-lookup"><span data-stu-id="4294f-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="4294f-181">A **dica de ferramenta Modo** de Inspeção agora indica se o elemento tem um nome e função acessíveis e é focalizado no [teclado][WebhintHintsAxeKeyboard]. [][WebhintHintsAxeNameRoleValue]</span><span class="sxs-lookup"><span data-stu-id="4294f-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="A dica de ferramenta Inspecionar Modo com informações de acessibilidade" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="4294f-183">A **dica de ferramenta Inspecionar Modo** com informações de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="4294f-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-184">Problema do Chromium [#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="4294f-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="4294f-185">Atualizações do painel de desempenho</span><span class="sxs-lookup"><span data-stu-id="4294f-185">Performance panel updates</span></span>  

#### <a name="view-total-blocking-time-information-in-the-footer"></a><span data-ttu-id="4294f-186">Exibir informações de Tempo de Bloqueio Total no rodapé</span><span class="sxs-lookup"><span data-stu-id="4294f-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="4294f-187">Depois de gravar seu desempenho de carga, o **painel Desempenho** agora mostra informações de Tempo de Bloqueio Total \(TBT\) no rodapé.</span><span class="sxs-lookup"><span data-stu-id="4294f-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="4294f-188">O TBT é uma métrica de desempenho de carga que ajuda a quantificar quanto tempo uma página leva para se tornar usável.</span><span class="sxs-lookup"><span data-stu-id="4294f-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="4294f-189">Ele mede basicamente por quanto tempo uma página parece ser usável \(porque o conteúdo é renderizado na tela\); mas não é realmente usável, porque JavaScript está bloqueando o thread principal e, portanto, a página não responde à entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="4294f-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="4294f-190">O TBT é a principal métrica para se aproximar do Primeiro Atraso de Entrada.</span><span class="sxs-lookup"><span data-stu-id="4294f-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="4294f-191">Para obter informações de Tempo de Bloqueio Total, não use o **fluxo** de trabalho de ícone da página Atualizar Página de Atualização ![ para registrar o desempenho da carga da ][ImageRefreshPageIcon] página.</span><span class="sxs-lookup"><span data-stu-id="4294f-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="4294f-192">Em vez disso, **selecione Record** Record icon ![ , recarrege manualmente a página, aguarde a página ser carregada e, ][ImageRecordIcon] em seguida, pare a gravação.</span><span class="sxs-lookup"><span data-stu-id="4294f-192">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="4294f-193">Se `Total Blocking Time: Unavailable` for exibido, o Microsoft Edge DevTools não obterá as informações necessárias dos dados de perfil interno no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4294f-193">If `Total Blocking Time: Unavailable` is displayed, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total de informações de Tempo de Bloqueio no rodapé de uma gravação de painel de desempenho" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="4294f-195">Total de informações de Tempo de Bloqueio no rodapé de uma **gravação de painel** de desempenho</span><span class="sxs-lookup"><span data-stu-id="4294f-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-196">Problema do Chromium [#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="4294f-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <a name="layout-shift-events-in-the-new-experience-section"></a><span data-ttu-id="4294f-197">Eventos de Layout Shift na nova seção Experiência</span><span class="sxs-lookup"><span data-stu-id="4294f-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="4294f-198">A nova **seção Experiência** do **painel Desempenho** ajuda você a detectar turnos de layout.</span><span class="sxs-lookup"><span data-stu-id="4294f-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="4294f-199">A Mudança cumulativa de Layout \(CLS\) é uma métrica que ajuda você a quantificar a instabilidade visual indesejada.</span><span class="sxs-lookup"><span data-stu-id="4294f-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="4294f-200">Escolha o **evento Layout Shift** para exibir os detalhes da mudança de layout no painel **Resumo.**</span><span class="sxs-lookup"><span data-stu-id="4294f-200">Choose the **Layout Shift** event to display the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="4294f-201">Passe o mouse nos **campos Movido de e** Movido **para** visualizar onde ocorreu a mudança de layout.</span><span class="sxs-lookup"><span data-stu-id="4294f-201">Hover on the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Os detalhes de uma mudança de layout" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="4294f-203">Os detalhes de uma mudança de layout</span><span class="sxs-lookup"><span data-stu-id="4294f-203">The details of a layout shift</span></span>  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a><span data-ttu-id="4294f-204">Terminologia de promessa mais precisa no Console</span><span class="sxs-lookup"><span data-stu-id="4294f-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="4294f-205">Ao registrar um `Promise` , o console **forneceu** o valor `PromiseStatus` incorretamente definido como `resolved` .</span><span class="sxs-lookup"><span data-stu-id="4294f-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Um exemplo do Console usando a terminologia resolvida antiga" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="4294f-207">Um exemplo do **Console** usando a `resolved` terminologia antiga</span><span class="sxs-lookup"><span data-stu-id="4294f-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-208">O **Console** agora usa o termo `fulfilled` , que se alinha à `Promise` especificação.</span><span class="sxs-lookup"><span data-stu-id="4294f-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="4294f-209">Para obter mais informações sobre a `Promise` especificação, navegue até [Estados e Destinos no GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="4294f-209">For more information about the `Promise` specification, navigate to [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Um exemplo do Console usando a nova terminologia cumprida" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="4294f-211">Um exemplo do **Console usando** a `fulfilled` nova terminologia</span><span class="sxs-lookup"><span data-stu-id="4294f-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-212">V8 issue [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="4294f-212">V8 issue [#6751][CRV86751]</span></span>  

### <a name="styles-pane-updates"></a><span data-ttu-id="4294f-213">Atualizações do painel estilos</span><span class="sxs-lookup"><span data-stu-id="4294f-213">Styles pane updates</span></span>  

#### <a name="support-for-the-revert-keyword"></a><span data-ttu-id="4294f-214">Suporte para a palavra-chave de reverter</span><span class="sxs-lookup"><span data-stu-id="4294f-214">Support for the revert keyword</span></span>  

<span data-ttu-id="4294f-215">A interface do usuário de preenchimento automático do painel **Estilos** agora detecta a palavra-chave [CSS][MDNRevert] revertida, que reverte o valor em cascata de uma propriedade para o valor anterior aplicado ao estilo do elemento.</span><span class="sxs-lookup"><span data-stu-id="4294f-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Definindo o valor de uma propriedade a ser revertida" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="4294f-217">Definindo o valor de uma propriedade a ser revertida</span><span class="sxs-lookup"><span data-stu-id="4294f-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-218">Problema do Chromium [#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="4294f-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <a name="image-previews"></a><span data-ttu-id="4294f-219">Visualizações de imagem</span><span class="sxs-lookup"><span data-stu-id="4294f-219">Image previews</span></span>  

<span data-ttu-id="4294f-220">Passe o mouse em um valor no painel Estilos para `background-image` exibir uma visualização da imagem em uma dica de ferramenta. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4294f-220">Hover on a `background-image` value in the **Styles** pane to display a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Passar o mouse sobre um valor de imagem em segundo plano" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="4294f-222">Passar o mouse sobre um `background-image` valor</span><span class="sxs-lookup"><span data-stu-id="4294f-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-223">Problema do Chromium [#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="4294f-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a><span data-ttu-id="4294f-224">O Selador de Cores agora usa notação de cor funcional separada por espaço</span><span class="sxs-lookup"><span data-stu-id="4294f-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="4294f-225">[O Módulo de Cor CSS Nível 4][CSSWGDraftsColor4Changes3] especifica que as funções de cor, como , devem dar suporte a `rgb()` argumentos separados por espaço.</span><span class="sxs-lookup"><span data-stu-id="4294f-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="4294f-226">Por exemplo, `rgb(0, 0, 0)` é equivalente a `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="4294f-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="4294f-227">Quando você escolhe [][DevtoolsCssReferenceColorPicker] cores com o Seletor de Cores ou alterna entre representações de cores no painel **Estilos** segurando e selecionando o valor, a sintaxe de argumento separada por espaço é `Shift` `background-color` exibida.</span><span class="sxs-lookup"><span data-stu-id="4294f-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, the space-separated argument syntax is displayed.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Usando argumentos separados por espaço no painel Estilos" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="4294f-229">Usando argumentos separados por espaço no painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="4294f-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="4294f-230">Você também deve exibir a sintaxe no painel **Computed** e na dica de ferramenta **Inspecionar Modo.**</span><span class="sxs-lookup"><span data-stu-id="4294f-230">You should also display the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="4294f-231">O Microsoft Edge DevTools está usando a nova sintaxe porque os recursos CSS futuros, como [color()][CSSWGDraftsColor4Property] não suportam a sintaxe de argumento preterida separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4294f-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="4294f-232">A sintaxe de argumento separada por espaço tem suporte na maioria dos navegadores por um tempo.</span><span class="sxs-lookup"><span data-stu-id="4294f-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="4294f-233">Para obter mais informações, navegue até [Posso usar: Notações][CaniuseMDNSpaceSeparatedFunctionalColorNotations] de cores funcionais separadas por espaço?</span><span class="sxs-lookup"><span data-stu-id="4294f-233">For more information, navigate to [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="4294f-234">Problema do Chromium [#1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="4294f-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a><span data-ttu-id="4294f-235">Deprecation do painel Propriedades no painel Elementos</span><span class="sxs-lookup"><span data-stu-id="4294f-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="4294f-236">O **painel Propriedades** na ferramenta **Elements** é preterido.</span><span class="sxs-lookup"><span data-stu-id="4294f-236">The **Properties** pane in the **Elements** tool is deprecated.</span></span>  <span data-ttu-id="4294f-237">Em `console.dir($0)` vez **disso, execute no Console.**</span><span class="sxs-lookup"><span data-stu-id="4294f-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="O painel Propriedades preterida" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="4294f-239">O painel Propriedades \*\*\*\* preterida</span><span class="sxs-lookup"><span data-stu-id="4294f-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <a name="references"></a><span data-ttu-id="4294f-240">Referências</span><span class="sxs-lookup"><span data-stu-id="4294f-240">References</span></span>  

*   [<span data-ttu-id="4294f-241">console.dir()</span><span class="sxs-lookup"><span data-stu-id="4294f-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="4294f-242">$0</span><span class="sxs-lookup"><span data-stu-id="4294f-242">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a><span data-ttu-id="4294f-243">Suporte a atalhos de aplicativo no painel Manifesto</span><span class="sxs-lookup"><span data-stu-id="4294f-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="4294f-244">Atalhos de aplicativo ajudam os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="4294f-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="4294f-245">O menu atalhos do aplicativo é mostrado apenas para Aplicativos [Web][PwaIndex] Progressivos instalados na área de trabalho ou dispositivo móvel do usuário.</span><span class="sxs-lookup"><span data-stu-id="4294f-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Atalhos de aplicativo no painel Manifesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="4294f-247">Atalhos de aplicativo no painel **Manifesto**</span><span class="sxs-lookup"><span data-stu-id="4294f-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="4294f-248">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4294f-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="4294f-249">Se você estiver no Windows ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="4294f-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="4294f-250">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="4294f-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="4294f-251">Entrar em contato com a equipe do Microsoft Edge Devtools</span><span class="sxs-lookup"><span data-stu-id="4294f-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Use o emulador do Surface Duo | Microsoft Docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir - Console API Reference | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento selecionado recentemente ou objeto JavaScript - Referência da API de Utilitários de Console | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Alterar cores com o Seletor de Cores - Referência CSS | Microsoft Docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta - Personalizar visão geral | Microsoft Docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Encontre e corrige problemas com a guia Problemas do Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Iniciar com emuladores do Surface Duo de Depuração Remota | Microsoft Docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Começar com a depuração remota de dispositivos Windows 10 | Microsoft Docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecione os detalhes do recurso | Microsoft Docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Log network activity | Microsoft Docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web Progressivos no Windows | Microsoft Docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicativo Do Microsoft Edge Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notações de cores funcionais separadas por espaço - MDN | Posso usar"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: Permitir personalizar atalhos de teclado/vinculações de teclas | Bugs do Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Bugs do Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: visualizar facilmente imagens e imagens de plano de fundo no painel Estilos | Bugs do Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: mostrar informações básicas do a11y no elemento | Bugs do Chromium"  
[CR1048378]: https://crbug.com/1048378 "Suporte à interface do usuário do DevTools para o modo de alto contraste | Bugs do Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Bugs do Chromium"  
[CR1068116]: https://crbug.com/1068116 "Painel de problemas de | Bugs do Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: o seletor de cores deve produzir uma sintaxe de cor CSS moderna | Bugs do Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: adicione suporte para a palavra-chave/valor css 'reverter' | Bugs do Chromium"  
[CR1076112]: https://crbug.com/1076112 "Personalização de devtools - resizer de gaveta"  
[CR1081486]: https://crbug.com/1081486 "Foco do teclado não visível para botões de navegação no modo screencast | Bugs do Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus deve ser 'cumprido', não 'resolvido' | Bugs de V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Alterações de Cores 3 - Css Color Module Level 4 | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Cor de primeiro plano: a "cor" - Css Color Module Level 4 | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Apresentando o novo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados e Destinos - domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "reverter | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidade do navegador | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Código"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio atalhos de teclado de código para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: teclado | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Ativar ou desativar o modo de alto contraste no Windows | Suporte ao Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema - MicrosoftDocs/desenvolvedor de borda"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="4294f-296">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4294f-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4294f-297">A página original é [encontrada](https://developers.google.com/web/updates/2020/05/devtools/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4294f-297">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4294f-299">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4294f-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
