---
description: Conheça as ferramentas de desenvolvedor do Microsoft Edge (EdgeHTML)
title: Ferramentas de desenvolvedor do Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629501"
---
# <span data-ttu-id="09bd8-104">Ferramentas de desenvolvedor do Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="09bd8-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

<span data-ttu-id="09bd8-105">Os DevTools Microsoft Edge \ (EdgeHTML \) são criados com [TypeScript][|::ref1::|Index], habilitados por [fonte aberta][GithubMicrosoftChakracore], otimizados para fluxos de trabalho de front-end modernos e agora disponíveis como um [aplicativo autônomo do Windows 10][MicrosoftStoreEdgeDevtoolsPreview] na Microsoft Store!</span><span class="sxs-lookup"><span data-stu-id="09bd8-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="09bd8-106">Para saber mais sobre os recursos mais recentes, confira [devtools na atualização mais recente do Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="09bd8-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="09bd8-107">Ferramentas principais</span><span class="sxs-lookup"><span data-stu-id="09bd8-107">Core tools</span></span>  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   <span data-ttu-id="09bd8-109">Microsoft Edge (EdgeHTML) DevTools</span><span class="sxs-lookup"><span data-stu-id="09bd8-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="09bd8-110">O DevTools Microsoft Edge \ (EdgeHTML \) inclui:</span><span class="sxs-lookup"><span data-stu-id="09bd8-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="09bd8-111">Um painel de [elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML e CSS, inspecionar Propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de MUTAção dom</span><span class="sxs-lookup"><span data-stu-id="09bd8-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="09bd8-112">Um [console][DevtoolsGuideEdgehtml|::ref3::|] para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós dom e executar JavaScript no contexto da janela ou do quadro selecionado</span><span class="sxs-lookup"><span data-stu-id="09bd8-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="09bd8-113">Um [depurador][DevtoolsGuideEdgehtml|::ref4::|] para depurar o código, definir inspeções e pontos de interrupção, editar seu código e inspecionar o armazenamento da Web e os caches de cookies</span><span class="sxs-lookup"><span data-stu-id="09bd8-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="09bd8-114">Um painel de [rede][DevtoolsGuideEdgehtml|::ref5::|] para monitorar e inspecionar solicitações e respostas da rede e do cache do navegador</span><span class="sxs-lookup"><span data-stu-id="09bd8-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="09bd8-115">Um painel de [desempenho][DevtoolsGuideEdgehtml|::ref6::|] para criar o perfil do tempo e dos recursos do sistema necessários para seu site</span><span class="sxs-lookup"><span data-stu-id="09bd8-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="09bd8-116">Um painel de [memória][DevtoolsGuideEdgehtml|::ref7::|] para medir o uso dos recursos de memória e comparar os instantâneos de heap em diferentes Estados do tempo de execução do código</span><span class="sxs-lookup"><span data-stu-id="09bd8-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="09bd8-117">Um painel de [armazenamento][DevtoolsGuideEdgehtml|::ref8::|] para inspecionar e gerenciar seu armazenamento da Web, IndexedDB, cookies e dados de cache</span><span class="sxs-lookup"><span data-stu-id="09bd8-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="09bd8-118">Um painel [funcionários de serviço][DevtoolsGuideEdgehtmlServiceworkers] para gerenciar e depurar seus trabalhadores de serviço</span><span class="sxs-lookup"><span data-stu-id="09bd8-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="09bd8-119">Um painel de [emulação][DevtoolsGuideEdgehtml|::ref9::|] para testar seu site com diferentes perfis de navegador, resoluções de tela e coordenadas de localização de GPS</span><span class="sxs-lookup"><span data-stu-id="09bd8-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="09bd8-120">Continue enviando seus [comentários e solicitações de recursos](#feedback)!</span><span class="sxs-lookup"><span data-stu-id="09bd8-120">Please keep sending your [feedback and feature requests](#feedback)!</span></span>  

> [!TIP]
> <span data-ttu-id="09bd8-121">[Teste no Microsoft Edge \ (EdgeHTML \) grátis de qualquer navegador][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="09bd8-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="09bd8-122">A equipe do Microsoft Edge é parceira com o [BrowserStack][BrowserstackEdgehtml] para oferecer testes automatizados e ativos no Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="09bd8-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="09bd8-123">Aplicativo da Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="09bd8-123">Microsoft Store app</span></span>  

<span data-ttu-id="09bd8-124">O **devtools Microsoft Edge \ (EdgeHTML \)** [agora está disponível][DevtoolsGuideEdgehtmlWhatsnew] como um [aplicativo autônomo do Windows 10 da Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], além da experiência de ferramenta no navegador \ (`F12`\).</span><span class="sxs-lookup"><span data-stu-id="09bd8-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="09bd8-125">Com a versão da loja vem um painel do **seletor** para anexar a abertura de destinos de página locais e remotos e um layout com guias para facilitar a alternância entre instâncias de devtools.</span><span class="sxs-lookup"><span data-stu-id="09bd8-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="09bd8-126">Depuração local</span><span class="sxs-lookup"><span data-stu-id="09bd8-126">Local debugging</span></span>  

<span data-ttu-id="09bd8-127">Para depurar uma página localmente, basta iniciar o aplicativo Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="09bd8-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="09bd8-128">O painel **local** do seletor exibe todos os processos de conteúdo ativos do EdgeHTML, incluindo guias do navegador Edge aberto, executando [PWAs][PwasEdgehtmlIndex] \`WWAHost.exe\` (processos \) e controles [WebView][HostingWebview] .</span><span class="sxs-lookup"><span data-stu-id="09bd8-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="09bd8-129">Selecione o destino desejado para anexar e abrir uma nova instância de guia do DevTools.</span><span class="sxs-lookup"><span data-stu-id="09bd8-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Painel local do aplicativo DevTools":::
   <span data-ttu-id="09bd8-131">Painel local do aplicativo DevTools</span><span class="sxs-lookup"><span data-stu-id="09bd8-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="09bd8-132">Depuração remota</span><span class="sxs-lookup"><span data-stu-id="09bd8-132">Remote debugging</span></span>  

<span data-ttu-id="09bd8-133">O aplicativo Microsoft Edge DevTools introduz suporte básico para depurar páginas em um computador remoto por meio do [protocolo devtools][DevtoolsProtocolEdgehtmlIndex]recém-lançado.</span><span class="sxs-lookup"><span data-stu-id="09bd8-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="09bd8-134">Com a versão mais recente vem o acesso remoto à funcionalidade central no [depurador][DevtoolsGuideEdgehtml|::ref10::|], [elementos][DevtoolsGuideEdgehtml|::ref11::|] \ (para operações somente leitura \) e painéis do [console][DevtoolsGuideEdgehtml|::ref12::|] .</span><span class="sxs-lookup"><span data-stu-id="09bd8-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="09bd8-135">A depuração remota está limitada ao Microsoft Edge \ (EdgeHTML \) que executa hosts de área de trabalho, com suporte para outros hosts EdgeHTML e dispositivos Windows 10 chegando em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="09bd8-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="09bd8-136">Para começar, confira a seção [*devtools do Microsoft Edge*][DevtoolsProtocolEdgehtmlClientsEdgePreview] dos documentos de [protocolo do devtools][DevtoolsProtocolEdgehtmlIndex] .</span><span class="sxs-lookup"><span data-stu-id="09bd8-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Painel remoto do aplicativo DevTools":::
   <span data-ttu-id="09bd8-138">Painel remoto do aplicativo DevTools</span><span class="sxs-lookup"><span data-stu-id="09bd8-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="09bd8-139">Atalhos gerais</span><span class="sxs-lookup"><span data-stu-id="09bd8-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="09bd8-140">Todos os atalhos foram verificados na versão mais recente do Windows.</span><span class="sxs-lookup"><span data-stu-id="09bd8-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="09bd8-141">Se não for possível usar um atalho, atualize sua cópia do Windows.</span><span class="sxs-lookup"><span data-stu-id="09bd8-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="09bd8-142">Esses atalhos controlam a janela principal do DevTools e devem funcionar em todas as ferramentas.</span><span class="sxs-lookup"><span data-stu-id="09bd8-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="09bd8-143">Ação</span><span class="sxs-lookup"><span data-stu-id="09bd8-143">Action</span></span> | <span data-ttu-id="09bd8-144">Atalho</span><span class="sxs-lookup"><span data-stu-id="09bd8-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="09bd8-145">Mostrar/ocultar DevTools \ (abre para o último painel exibido \)</span><span class="sxs-lookup"><span data-stu-id="09bd8-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="09bd8-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="09bd8-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="09bd8-147">Alternar encaixe \ (desencaixar/abaixo/direita \)</span><span class="sxs-lookup"><span data-stu-id="09bd8-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="09bd8-148">Abrir arquivo</span><span class="sxs-lookup"><span data-stu-id="09bd8-148">Open file</span></span> | `Ctrl`<span data-ttu-id="09bd8-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="09bd8-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="09bd8-150">Mostrar código-fonte HTML não editável no depurador</span><span class="sxs-lookup"><span data-stu-id="09bd8-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="09bd8-151">Mostrar/ocultar console na parte inferior de qualquer outra ferramenta</span><span class="sxs-lookup"><span data-stu-id="09bd8-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="09bd8-152">Alternar para elementos \ (explorador do DOM \)</span><span class="sxs-lookup"><span data-stu-id="09bd8-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="09bd8-153">Alternar para o console</span><span class="sxs-lookup"><span data-stu-id="09bd8-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="09bd8-154">Alternar para o depurador</span><span class="sxs-lookup"><span data-stu-id="09bd8-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="09bd8-155">Alternar para a rede</span><span class="sxs-lookup"><span data-stu-id="09bd8-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="09bd8-156">Alternar para o desempenho</span><span class="sxs-lookup"><span data-stu-id="09bd8-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="09bd8-157">Alternar para memória</span><span class="sxs-lookup"><span data-stu-id="09bd8-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="09bd8-158">Alternar para emulação</span><span class="sxs-lookup"><span data-stu-id="09bd8-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="09bd8-159">Documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="09bd8-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="09bd8-160">Próxima ferramenta</span><span class="sxs-lookup"><span data-stu-id="09bd8-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="09bd8-161">Ferramenta anterior</span><span class="sxs-lookup"><span data-stu-id="09bd8-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="09bd8-162">Ferramenta anterior \ (do histórico \)</span><span class="sxs-lookup"><span data-stu-id="09bd8-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="09bd8-163">Próxima ferramenta \ (do histórico \)</span><span class="sxs-lookup"><span data-stu-id="09bd8-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="09bd8-164">Subquadro seguinte</span><span class="sxs-lookup"><span data-stu-id="09bd8-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="09bd8-165">Subquadro anterior</span><span class="sxs-lookup"><span data-stu-id="09bd8-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="09bd8-166">Próxima correspondência na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="09bd8-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="09bd8-167">Correspondência anterior na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="09bd8-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="09bd8-168">Localizar na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="09bd8-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="09bd8-169">Coloque o foco no console na parte inferior</span><span class="sxs-lookup"><span data-stu-id="09bd8-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="09bd8-170">Iniciar o DevTools para o console</span><span class="sxs-lookup"><span data-stu-id="09bd8-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="09bd8-171">Atualizar a página</span><span class="sxs-lookup"><span data-stu-id="09bd8-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="09bd8-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="09bd8-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="09bd8-173">Se você estiver Depurando e pausado em um ponto de interrupção, a ação **atualizar a página** retomará o tempo de execução primeiro.</span><span class="sxs-lookup"><span data-stu-id="09bd8-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="09bd8-174">Privacidade Jurídica</span><span class="sxs-lookup"><span data-stu-id="09bd8-174">Feedback</span></span>  

<span data-ttu-id="09bd8-175">Envie seus comentários para ajudar a melhorar o Microsoft Edge \ (EdgeHTML \) DevTools para você!</span><span class="sxs-lookup"><span data-stu-id="09bd8-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="09bd8-176">Basta abrir as ferramentas \ (`F12`\) e selecionar o botão [enviar comentários](#microsoft-edge-edgehtml-developer-tools) .</span><span class="sxs-lookup"><span data-stu-id="09bd8-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="09bd8-177">Torne-se um [Windows Insider][WindowsInsiderProgram] para visualizar os [recursos mais recentes que chegam ao devtools][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="09bd8-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="09bd8-178">Use o aplicativo Hub de feedback do Windows para postar, fazer uma votação, acompanhar e obter suporte para sugestões gerais do Windows e problemas.</span><span class="sxs-lookup"><span data-stu-id="09bd8-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Consola"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulação"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Rowset"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Network"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Execução"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Trabalhadores do serviço"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "SPS"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo de DevTools Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clientes do protocolo DevTools preview do Microsoft Edge-DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) para aplicativos do Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicativos Web progressivos (EdgeHTML) no Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools Preview"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste do navegador Microsoft Edge gratuito | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
