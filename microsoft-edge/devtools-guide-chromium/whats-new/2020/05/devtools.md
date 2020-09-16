---
description: Use o DevTools no modo de alto contraste do Windows, CORRESP os atalhos de teclado no código do DevTools para o Visual Studio e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2752dec8bc7c4eec34ddde05a7dedff7bebef05f
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015486"
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

# <span data-ttu-id="bd559-104">O que há de novo no DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="bd559-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <span data-ttu-id="bd559-105">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bd559-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="bd559-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="bd559-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="bd559-107">Dê uma olhada neles para experimentar novos recursos no DevTools, extensões de código do Visual Studio e muito mais.</span><span class="sxs-lookup"><span data-stu-id="bd559-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="bd559-108">Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="bd559-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="bd559-109">Usar o DevTools no modo de alto contraste do Windows</span><span class="sxs-lookup"><span data-stu-id="bd559-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="bd559-110">O Microsoft Edge DevTools agora é exibido no modo de alto contraste quando o Windows está no modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="bd559-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="O Microsoft Edge DevTools no modo de alto contraste" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="bd559-112">O Microsoft Edge DevTools no modo de alto contraste</span><span class="sxs-lookup"><span data-stu-id="bd559-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-113">[Siga as instruções para ativar o modo de alto contraste no Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="bd559-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="bd559-114">Abra o DevTools no Microsoft Edge pressionando `F12` ou `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="bd559-114">Open the DevTools in Microsoft Edge by pressing `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="bd559-115">O DevTools é exibido no modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="bd559-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="bd559-116">O Microsoft Edge DevTools atualmente é compatível com o modo de alto contraste no Windows, mas não no macOS.</span><span class="sxs-lookup"><span data-stu-id="bd559-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span> 

<span data-ttu-id="bd559-117">Chromium problema [#1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="bd559-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <span data-ttu-id="bd559-118">Corresponder os atalhos de teclado no código do DevTools para o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bd559-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="bd559-119">Do seu [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) e do [controlador de problemas Chromium público][CRIssuesList], a equipe do Microsoft Edge devtools aprendeu que você queria a capacidade de personalizar atalhos de teclado no devtools.</span><span class="sxs-lookup"><span data-stu-id="bd559-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="bd559-120">No Microsoft Edge 84, agora você pode fazer a correspondência entre os atalhos de teclado no código do DevTools para o [Visual Studio][VSCode], que é apenas um dos recursos nos quais a equipe está trabalhando para a personalização de atalhos.</span><span class="sxs-lookup"><span data-stu-id="bd559-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VSCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="bd559-122">O Microsoft Edge DevTools no modo de alto contraste</span><span class="sxs-lookup"><span data-stu-id="bd559-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-123">Para experimentar o experimento, abra as configurações do DevTools pressionando `?` ou selecionando o ícone de ![ configurações do devtools ][ImageSettingsIcon] no canto superior direito da devtools.</span><span class="sxs-lookup"><span data-stu-id="bd559-123">To try the experiment, open DevTools Settings by pressing `?` or selecting the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="bd559-124">Navegue até a seção **experimentos** e marque **habilitar a guia Configurações de atalhos de teclado personalizados (requer recarregamento)**.</span><span class="sxs-lookup"><span data-stu-id="bd559-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="bd559-125">Agora, recarregue o DevTools, abra as configurações novamente e navegue até a seção **atalhos** .</span><span class="sxs-lookup"><span data-stu-id="bd559-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="bd559-126">Selecione **devtools (padrão)** na lista suspensa **coincidir os atalhos de predefinir** e selecione **código do Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="bd559-126">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="bd559-127">Os atalhos de teclado no DevTools agora correspondem aos atalhos para ações equivalentes no código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bd559-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="bd559-128">Por exemplo, o atalho de teclado para pausar ou continuar a execução de um script no [código do Visual Studio][VSCodeShortcuts] é `F5` .</span><span class="sxs-lookup"><span data-stu-id="bd559-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VSCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="bd559-129">Com a predefinição **devtools (padrão)** , o mesmo atalho no devtools está, `F8` mas com a predefinição de **código do Visual Studio** , esse atalho também é `F5` .</span><span class="sxs-lookup"><span data-stu-id="bd559-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="bd559-130">No momento, o recurso está disponível no Microsoft Edge 84 como um experimento, portanto Compartilhe seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team) com a equipe!</span><span class="sxs-lookup"><span data-stu-id="bd559-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="bd559-131">Chromium problema [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="bd559-131">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="bd559-132">Emuladores Remote Debug Surface Duo</span><span class="sxs-lookup"><span data-stu-id="bd559-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="bd559-133">Agora você pode depurar remotamente o conteúdo da Web em execução no [emulador Surface Duo][DualScreensAndroidEmulator] usando toda a capacidade do [Microsoft Edge devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="bd559-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="bd559-134">Com o [emulador Surface Duo][DualScreensAndroidEmulator], você pode testar como o conteúdo da Web é renderizado em uma nova classe de dispositivos dobrável e de tela dupla.</span><span class="sxs-lookup"><span data-stu-id="bd559-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="bd559-135">O emulador executa o sistema operacional Android e fornece o [aplicativo Android do Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="bd559-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="bd559-136">Carregue o conteúdo da Web no [aplicativo Microsoft Edge][AndroidEdge] e depure-o com o [Microsoft Edge devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="bd559-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="O aplicativo Microsoft Edge em execução no emulador Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="bd559-138">O aplicativo Microsoft Edge no emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="bd559-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-139">A `edge://inspect` página em uma instância da área de trabalho do [Microsoft Edge][DesktopEdge] mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][PwaIndex] que estão em execução no [emulador Surface Duo][DualScreensAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="bd559-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="A página edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="bd559-141">A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador</span><span class="sxs-lookup"><span data-stu-id="bd559-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="bd559-142">Selecionar **inspecionar** para a guia ou PWA que você deseja depurar abre o [Microsoft Edge devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="bd559-142">Selecting **inspect** for the tab or PWA that you want to debug opens the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="bd559-143">[Siga o guia passo a passo para depurar remotamente o conteúdo da Web no emulador Surface Duo][DevToolsRemoteDebugDuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="bd559-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <span data-ttu-id="bd559-144">Redimensionar a gaveta DevTools mais facilmente</span><span class="sxs-lookup"><span data-stu-id="bd559-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="bd559-145">No Microsoft Edge 83 ou anterior, você foi capaz de redimensionar a [gaveta devtools][DevToolsDrawer] passando dentro da barra de ferramentas da gaveta.</span><span class="sxs-lookup"><span data-stu-id="bd559-145">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the Drawer's toolbar.</span></span>  <span data-ttu-id="bd559-146">A gaveta se comportada de maneira diferente dos outros controles de redimensionamento para painéis no DevTools onde você passa o mouse sobre a borda do painel para redimensioná-lo.</span><span class="sxs-lookup"><span data-stu-id="bd559-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover over the border of the pane to resize it.</span></span>  <span data-ttu-id="bd559-147">Selecione a imagem a seguir para ver como o redimensionamento da gaveta trabalhou na versão 83 ou anterior do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bd559-147">Select the following image to see how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Redimensionando a gaveta DevTools no Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="bd559-149">Redimensionando a gaveta DevTools no Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="bd559-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="bd559-150">Começando com o Microsoft Edge 84, agora você pode redimensionar a gaveta passando o mouse sobre a borda da gaveta.</span><span class="sxs-lookup"><span data-stu-id="bd559-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="bd559-151">Essa alteração alinha o comportamento redimensionando a gaveta DevTools com a maneira como você redimensiona outros painéis no DevTools.</span><span class="sxs-lookup"><span data-stu-id="bd559-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="bd559-152">Selecione a imagem a seguir para ver o redimensionamento em ação no Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="bd559-152">Select the following image to see resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Redimensionando a gaveta DevTools no Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="bd559-154">Redimensionando a gaveta DevTools no Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="bd559-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="bd559-155">Chromium problema [#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="bd559-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <span data-ttu-id="bd559-156">Botões de navegação de screencasts exibem o foco</span><span class="sxs-lookup"><span data-stu-id="bd559-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="bd559-157">Ao depurar remotamente um [dispositivo Android][DevToolsRemoteDebugAndroid], um [dispositivo com o Windows 10][DevToolsRemoteDebugWindows]ou um [emulador Surface Duo][DevToolsRemoteDebugDuoEmulator], você pode alternar o screencast com o ![ ícone alternar screencast ][ImageScreencastingIcon] no canto superior esquerdo da devtools.</span><span class="sxs-lookup"><span data-stu-id="bd559-157">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="bd559-158">Com o screencast habilitado, você poderá navegar na guia no Microsoft Edge no dispositivo remoto na janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="bd559-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="bd559-159">No Microsoft Edge 84, esses botões de navegação agora também são acessíveis pelo teclado.</span><span class="sxs-lookup"><span data-stu-id="bd559-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Pressionar Shift + Tab na barra de URL do screencast mostra o foco no botão atualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="bd559-161">Pressione `Shift` + `Tab` a barra de URL com o screencast para mostrar o foco no botão **Atualizar**</span><span class="sxs-lookup"><span data-stu-id="bd559-161">Pressing `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="bd559-162">Chromium problema [#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="bd559-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <span data-ttu-id="bd559-163">O painel de detalhes do painel de rede agora está acessível</span><span class="sxs-lookup"><span data-stu-id="bd559-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="bd559-164">No Microsoft Edge 84, o [painel de detalhes][DevToolsNetworkDetails] no painel de **rede** agora tem foco quando você o abre para um recurso no [log de rede][DevToolsNetworkLog].</span><span class="sxs-lookup"><span data-stu-id="bd559-164">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** panel now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="bd559-165">Essa alteração permite que os leitores de tela leiam e interajam com o conteúdo do painel de **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="bd559-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="O painel de detalhes no painel rede tem o foco quando aberto" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="bd559-167">O painel de **detalhes** no painel **rede** tem o foco quando aberto</span><span class="sxs-lookup"><span data-stu-id="bd559-167">The **Details** pane in the **Network** panel takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="bd559-168">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="bd559-168">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="bd559-169">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="bd559-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="bd559-170">As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 84 que contribuíram para o projeto de código-fonte aberto Chromium.</span><span class="sxs-lookup"><span data-stu-id="bd559-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="bd559-171">Corrigir problemas de site com a nova ferramenta problemas na gaveta do DevTools</span><span class="sxs-lookup"><span data-stu-id="bd559-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="bd559-172">A nova ferramenta de **problemas** na gaveta devtools foi criada para ajudar a reduzir o cansativo de notificação e o email secundário do **console**.</span><span class="sxs-lookup"><span data-stu-id="bd559-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="bd559-173">Atualmente, o **console** é o local central para desenvolvedores de site, bibliotecas, estruturas e Microsoft Edge para registrar mensagens, avisos e erros.</span><span class="sxs-lookup"><span data-stu-id="bd559-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="bd559-174">A ferramenta **problemas** agrega avisos do navegador em uma maneira estruturada, agregada e acionável, links para recursos afetados no Microsoft Edge devtools e fornece orientação sobre como corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="bd559-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="bd559-175">Ao longo do tempo, você deve ver mais e mais avisos no Microsoft Edge faceamento na ferramenta **problemas** em vez de no **console**, o que pode ajudar a reduzir o email secundário no **console**.</span><span class="sxs-lookup"><span data-stu-id="bd559-175">Over time, you should see more and more warnings in Microsoft Edge surfacing in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="bd559-176">Para começar, confira [Localizar e corrigir problemas com a ferramenta problemas do Microsoft Edge devtools][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="bd559-176">To get started, see [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="A ferramenta problemas na gaveta DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="bd559-178">A ferramenta **problemas** na gaveta devtools</span><span class="sxs-lookup"><span data-stu-id="bd559-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-179">Chromium problema [#1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="bd559-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <span data-ttu-id="bd559-180">Exibir informações de acessibilidade na dica de ferramenta do modo de inspeção</span><span class="sxs-lookup"><span data-stu-id="bd559-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="bd559-181">A dica de ferramenta do **modo de inspeção** agora indica se o elemento tem um [nome e função][WebhintHintsAxeNameRoleValue] acessível e se é [focado no teclado][WebhintHintsAxeKeyboard].</span><span class="sxs-lookup"><span data-stu-id="bd559-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Dica de ferramenta do modo de inspeção com informações de acessibilidade" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="bd559-183">Dica de ferramenta do **modo de inspeção** com informações de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="bd559-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-184">Chromium problema [#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="bd559-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <span data-ttu-id="bd559-185">Atualizações do painel de desempenho</span><span class="sxs-lookup"><span data-stu-id="bd559-185">Performance panel updates</span></span>  

#### <span data-ttu-id="bd559-186">Exibir informações de tempo de bloqueio total no rodapé</span><span class="sxs-lookup"><span data-stu-id="bd559-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="bd559-187">Depois de gravar o desempenho da carga, o painel **desempenho** agora mostra as informações do tempo de bloqueio total \ (TBT \) no rodapé.</span><span class="sxs-lookup"><span data-stu-id="bd559-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="bd559-188">TBT é uma métrica de desempenho de carga que ajuda a quantificar o tempo que uma página leva para ser utilizável.</span><span class="sxs-lookup"><span data-stu-id="bd559-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="bd559-189">Isso essencialmente mede o tempo em que uma página parece ser utilizável \ (porque o conteúdo é renderizado na tela \); Mas não é utilizável realmente porque o JavaScript está bloqueando o thread principal e, portanto, a página não responde à entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd559-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="bd559-190">TBT é a métrica principal para approximating do primeiro atraso de entrada.</span><span class="sxs-lookup"><span data-stu-id="bd559-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="bd559-191">Para obter informações sobre o tempo total de bloqueio, não use o fluxo de trabalho **Atualizar** ![ ícone da página ][ImageRefreshPageIcon] de atualização de página para gravar o desempenho da carga da página.</span><span class="sxs-lookup"><span data-stu-id="bd559-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="bd559-192">Em vez disso **, selecione** ![ o ícone registro ][ImageRecordIcon] de registro, recarregue manualmente a página, aguarde até que a página seja carregada e, em seguida, pare a gravação.</span><span class="sxs-lookup"><span data-stu-id="bd559-192">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="bd559-193">Se você vir `Total Blocking Time: Unavailable` , o Microsoft Edge devtools não obteve as informações necessárias dos dados internos de criação de perfil no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bd559-193">If you see `Total Blocking Time: Unavailable`, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total de informações de tempo de bloqueio no rodapé de uma gravação de painel de desempenho" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="bd559-195">Total de informações de tempo de bloqueio no rodapé de uma gravação de painel de **desempenho**</span><span class="sxs-lookup"><span data-stu-id="bd559-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-196">Chromium problema [#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="bd559-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <span data-ttu-id="bd559-197">Eventos Shift de layout na seção nova experiência</span><span class="sxs-lookup"><span data-stu-id="bd559-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="bd559-198">A seção **experiência** nova do painel **desempenho** ajuda você a detectar turnos de layout.</span><span class="sxs-lookup"><span data-stu-id="bd559-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="bd559-199">O deslocamento de layout cumulativo \ (CLS \) é uma métrica que ajuda você a quantificar a instabilidade Visual indesejada.</span><span class="sxs-lookup"><span data-stu-id="bd559-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="bd559-200">Selecione o evento de **deslocamento de layout** para ver os detalhes do deslocamento de layout no painel **Resumo** .</span><span class="sxs-lookup"><span data-stu-id="bd559-200">Select the **Layout Shift** event to see the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="bd559-201">Passe o mouse sobre os campos **movido de** e **movido para** para visualizar onde a mudança de layout ocorreu.</span><span class="sxs-lookup"><span data-stu-id="bd559-201">Hover over the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Os detalhes de uma mudança de layout" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="bd559-203">Os detalhes de uma mudança de layout</span><span class="sxs-lookup"><span data-stu-id="bd559-203">The details of a layout shift</span></span>  
:::image-end:::  

### <span data-ttu-id="bd559-204">Terminologia Promise mais precisa no console</span><span class="sxs-lookup"><span data-stu-id="bd559-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="bd559-205">Ao registrar um `Promise` , o valor de **console** fornecido incorretamente é `PromiseStatus` definido como `resolved` .</span><span class="sxs-lookup"><span data-stu-id="bd559-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Um exemplo do console usando a antiga terminologia resolvida" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="bd559-207">Um exemplo do **console** que usa a antiga `resolved` terminologia</span><span class="sxs-lookup"><span data-stu-id="bd559-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-208">O **console** agora usa o termo `fulfilled` , que se alinha com a `Promise` especificação.</span><span class="sxs-lookup"><span data-stu-id="bd559-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="bd559-209">Para obter mais informações sobre a `Promise` especificação, consulte [Estados e Fates no GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="bd559-209">For more information about the `Promise` specification, see [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Um exemplo do console usando a nova terminologia atendida" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="bd559-211">Um exemplo do **console** usando a nova `fulfilled` terminologia</span><span class="sxs-lookup"><span data-stu-id="bd559-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-212">V8 problema [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="bd559-212">V8 issue [#6751][CRV86751]</span></span>  

### <span data-ttu-id="bd559-213">Atualizações do painel de estilos</span><span class="sxs-lookup"><span data-stu-id="bd559-213">Styles pane updates</span></span>  

#### <span data-ttu-id="bd559-214">Suporte para a palavra-chave REVERT</span><span class="sxs-lookup"><span data-stu-id="bd559-214">Support for the revert keyword</span></span>  

<span data-ttu-id="bd559-215">A interface do usuário de autocompletar do painel **estilos** agora detecta a palavra-chave CSS [REVERT][MDNRevert] , que reverte o valor em cascata de uma propriedade para o valor anterior aplicado ao estilo do elemento.</span><span class="sxs-lookup"><span data-stu-id="bd559-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Definir o valor de uma propriedade para reverter" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="bd559-217">Definir o valor de uma propriedade para reverter</span><span class="sxs-lookup"><span data-stu-id="bd559-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-218">Chromium problema [#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="bd559-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <span data-ttu-id="bd559-219">Visualizações de imagens</span><span class="sxs-lookup"><span data-stu-id="bd559-219">Image previews</span></span>  

<span data-ttu-id="bd559-220">Passe o mouse sobre um `background-image` valor no painel **estilos** para ver uma visualização da imagem em uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="bd559-220">Hover over a `background-image` value in the **Styles** pane to see a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Passando o cursor do mouse sobre um valor de imagem de tela de fundo" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="bd559-222">Passar o mouse sobre um `background-image` valor</span><span class="sxs-lookup"><span data-stu-id="bd559-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-223">Chromium problema [#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="bd559-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <span data-ttu-id="bd559-224">Agora, o seletor de cores usa a notação de cores funcional separada por espaços</span><span class="sxs-lookup"><span data-stu-id="bd559-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="bd559-225">[Módulo de cores CSS nível 4][CSSWGDraftsColor4Changes3] especifica que as funções de cor, como, por exemplo `rgb()` , devem dar suporte a argumentos separados por espaço.</span><span class="sxs-lookup"><span data-stu-id="bd559-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="bd559-226">Por exemplo, `rgb(0, 0, 0)` é equivalente a `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="bd559-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="bd559-227">Ao escolher as cores com o [seletor de cores][DevtoolsCssReferenceColorPicker] ou alternar entre as representações de cores no painel **estilos** , mantendo `Shift` e selecionando o `background-color` valor, você verá a sintaxe do argumento separado por espaços.</span><span class="sxs-lookup"><span data-stu-id="bd559-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, you should see the space-separated argument syntax.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Usando argumentos separados por espaço no painel estilos" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="bd559-229">Usando argumentos separados por espaço no painel **estilos**</span><span class="sxs-lookup"><span data-stu-id="bd559-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="bd559-230">Você também deve ver a sintaxe no painel **calculado** e a dica de ferramenta do **modo de inspeção** .</span><span class="sxs-lookup"><span data-stu-id="bd559-230">You should also see the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="bd559-231">O Microsoft Edge DevTools está usando a nova sintaxe porque recursos CSS futuros, como [Color ()][CSSWGDraftsColor4Property] , não são compatíveis com a sintaxe do argumento separado por vírgulas substituídas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="bd559-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="bd559-232">A sintaxe do argumento separado por espaços tem suporte na maioria dos navegadores há algum tempo.</span><span class="sxs-lookup"><span data-stu-id="bd559-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="bd559-233">Para obter mais informações, consulte [posso usar: notações de cores funcionais separadas por espaços?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="bd559-233">For more information, see [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="bd559-234">Chromium problema [#1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="bd559-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <span data-ttu-id="bd559-235">Substituição do painel Propriedades no painel elementos</span><span class="sxs-lookup"><span data-stu-id="bd559-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="bd559-236">O painel **Propriedades** no painel **elementos** é preterido.</span><span class="sxs-lookup"><span data-stu-id="bd559-236">The **Properties** pane in the **Elements** panel is deprecated.</span></span>  <span data-ttu-id="bd559-237">`console.dir($0)`Em vez disso, execute no **console** .</span><span class="sxs-lookup"><span data-stu-id="bd559-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="O painel Propriedades preteridas" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="bd559-239">O painel **Propriedades** preteridas</span><span class="sxs-lookup"><span data-stu-id="bd559-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <span data-ttu-id="bd559-240">Referências</span><span class="sxs-lookup"><span data-stu-id="bd559-240">References</span></span>  

*   [<span data-ttu-id="bd559-241">console. dir ()</span><span class="sxs-lookup"><span data-stu-id="bd559-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="bd559-242">$0</span><span class="sxs-lookup"><span data-stu-id="bd559-242">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <span data-ttu-id="bd559-243">Suporte a atalhos do aplicativo no painel manifesto</span><span class="sxs-lookup"><span data-stu-id="bd559-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="bd559-244">Os atalhos do aplicativo ajudam os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="bd559-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="bd559-245">O menu de atalhos do aplicativo é mostrado somente para [aplicativos Web progressivos][PwaIndex] que são instalados na área de trabalho do usuário ou no dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="bd559-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Atalhos do aplicativo no painel manifesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="bd559-247">Atalhos do aplicativo no painel **manifesto**</span><span class="sxs-lookup"><span data-stu-id="bd559-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="bd559-248">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bd559-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="bd559-249">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="bd559-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="bd559-250">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="bd559-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="bd559-251">Como entrar em contato com o Microsoft Edge devtools equipe</span><span class="sxs-lookup"><span data-stu-id="bd559-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Use o emulador Surface Duo | Documentos da Microsoft"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Dir-referência de API do console | Documentos da Microsoft"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento JavaScript ou elemento JavaScript selecionado recentemente-referência de API de utilitários de console | Documentos da Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Alterar as cores com o seletor de cores – referência de CSS | Documentos da Microsoft"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar visão geral | Documentos da Microsoft"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Localizar e corrigir problemas com a guia problemas do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introdução à depuração remota de dispositivos Android | Documentos da Microsoft"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Introdução aos emuladores Remote Debugging Surface Duo | Documentos da Microsoft"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introdução à depuração remota de dispositivos Windows 10 | Documentos da Microsoft"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecione os detalhes do recurso | Documentos da Microsoft"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar atividades da rede | Documentos da Microsoft"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows | Documentos da Microsoft"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicativo Android do Microsoft Edge"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notações de cores funcionais separadas por espaços-MDN | Posso usar"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: permite personalizar atalhos de teclado/associações de teclas | Erros de Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com a WCAG | Erros de Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: visualize facilmente imagens de plano de fundo e imagens no painel estilos | Erros de Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: show Basic A11y info in Element popover | Erros de Chromium"  
[CR1048378]: https://crbug.com/1048378 "Suporte de interface do usuário DevTools para modo de alto contraste | Erros de Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Erros de Chromium"  
[CR1068116]: https://crbug.com/1068116 "Painel de envio de problemas | Erros de Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: o seletor de cores deve produzir uma sintaxe de cor CSS moderna | Erros de Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: adicionar suporte para a palavra-chave/valor da CSS ' rever ' | Erros de Chromium"  
[CR1076112]: https://crbug.com/1076112 "Personalização de devtools-redimensionador de gaveta"  
[CR1081486]: https://crbug.com/1081486 "O foco do teclado não está visível para botões de navegação no modo screencast | Erros de Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus deve ser ' cumprido ', não ' resolvido ' | Erros de V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Alterações de cores 3-módulo de cor CSS nível 4 | Rascunhos do editor de grupo de trabalho W3C CSS"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. cor do primeiro plano: ' cor '-nível 4 do módulo colorido CSS | Rascunhos do editor de grupo de trabalho W3C CSS"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Apresentando o novo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados e Fates-Domenic/promessas-desempacotamento | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "reverter | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidade com o navegador | MDN"  

[VSCode]: https://code.visualstudio.com/ "Código do Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Atalhos de teclado de código do Visual Studio para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: teclado | Webhint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: nome função valor | Webhint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Ativar ou desativar o modo de alto contraste no Windows | Suporte do Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  
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
> <span data-ttu-id="bd559-296">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="bd559-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bd559-297">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/05/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="bd559-297">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bd559-299">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bd559-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
