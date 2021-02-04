---
description: Conhecer as Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)
title: Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 89fdbcdf10d10c57836067ca7d02afa3fd48cbc9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231481"
---
# <span data-ttu-id="29621-104">Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="29621-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](../includes/new-devtools-version-note.md)]  

<span data-ttu-id="29621-105">As Ferramentas para Desenvolvedores do Microsoft Edge \(EdgeHTML\) são criadas com o TypeScript, da plataforma[software livre][GithubMicrosoftChakracore], otimizadas para fluxos de trabalho front-end modernos, e agora disponíveis como um[aplicativo autônomo Windows 10][MicrosoftStoreEdgeDevtoolsPreview] na Microsoft Store!</span><span class="sxs-lookup"><span data-stu-id="29621-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="29621-106">Para saber mais sobre os recursos mais recentes, confira [DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="29621-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="29621-107">Ferramentas principais</span><span class="sxs-lookup"><span data-stu-id="29621-107">Core tools</span></span>  

:::image type="complex" source="./media/devtools.png" alt-text="Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)":::
   <span data-ttu-id="29621-109">Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="29621-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="29621-110">As Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML) incluem:</span><span class="sxs-lookup"><span data-stu-id="29621-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="29621-111">Um painel de [Elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML e CSS, inspecionar propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de mutação do DOM.</span><span class="sxs-lookup"><span data-stu-id="29621-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="29621-112">Um [Console][DevtoolsGuideEdgehtml|::ref3::|] para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós do DOM e executar o JavaScript no contexto da janela ou quadro selecionado.</span><span class="sxs-lookup"><span data-stu-id="29621-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="29621-113">Um [Depurador][DevtoolsGuideEdgehtml|::ref4::|] para percorrer o código, definir inspeções e pontos de interrupção, editar seu código ao vivo e inspecionar o armazenamento da Web e os caches de cookies</span><span class="sxs-lookup"><span data-stu-id="29621-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="29621-114">Um painel de[Rede][DevtoolsGuideEdgehtml|::ref5::|]para monitorar e inspecionar solicitações e respostas do cache da rede e do navegador</span><span class="sxs-lookup"><span data-stu-id="29621-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="29621-115">Um painel de [Desempenho][DevtoolsGuideEdgehtml|::ref6::|] para criar um perfil de tempo e recursos do sistema necessários para o seu site</span><span class="sxs-lookup"><span data-stu-id="29621-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="29621-116">Um painel de [Memória][DevtoolsGuideEdgehtml|::ref7::|] para medir o uso dos recursos de memória e comparar os instantâneos da pilha em diferentes estados de tempo de execução do código</span><span class="sxs-lookup"><span data-stu-id="29621-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="29621-117">Um painel de[Armazenamento][DevtoolsGuideEdgehtml|::ref8::|] para inspecionar e gerenciar seu armazenamento na Web, IndexedDB, cookies e dados de cache</span><span class="sxs-lookup"><span data-stu-id="29621-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="29621-118">Um painel de [Profissionais de Serviço][DevtoolsGuideEdgehtmlServiceworkers] para gerenciar e depurar seus profissionais de serviço.</span><span class="sxs-lookup"><span data-stu-id="29621-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="29621-119">Um painel de [Emulação][DevtoolsGuideEdgehtml|::ref9::|] para testar o seu site com diferentes perfis de navegador, resoluções de tela e coordenadas de localização do GPS</span><span class="sxs-lookup"><span data-stu-id="29621-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="29621-120">Continue enviando seus [comentários e solicitações de recursos](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span><span class="sxs-lookup"><span data-stu-id="29621-120">Please keep sending your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>  

> [!TIP]
> <span data-ttu-id="29621-121">[Teste no Microsoft Edge \(EdgeHTML\) gratuitamente em qualquer navegador][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="29621-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="29621-122">A equipe do Microsoft Edge criou uma parceria com o [BrowserStack][BrowserstackEdgehtml] para fornecer testes gratuitos e automatizados no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="29621-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="29621-123">Aplicativo da Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="29621-123">Microsoft Store app</span></span>  

<span data-ttu-id="29621-124">As **Ferramentas para Desenvolvedores do Microsoft Edge \(EdgeHTML\)** estão [disponíveis agora][DevtoolsGuideEdgehtmlWhatsnew] como um aplicativo autônomo [Windows 10 da Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], além da experiência de ferramentas do navegador \(`F12`\).</span><span class="sxs-lookup"><span data-stu-id="29621-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="29621-125">Com a versão da loja, há um painel de **seletor** para anexar a abrir destinos de página locais e remotos e um layout com guias para alternar entre instâncias das DevTools.</span><span class="sxs-lookup"><span data-stu-id="29621-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="29621-126">Depuração local</span><span class="sxs-lookup"><span data-stu-id="29621-126">Local debugging</span></span>  

<span data-ttu-id="29621-127">Para depurar uma página localmente, basta iniciar o aplicativo Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="29621-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="29621-128">O painel **Local** do seletor exibirá todos os processos de conteúdo ativos do EdgeHTML, incluindo as guias de navegação abertas do Edge, [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processos\) em funcionamento e [controles][HostingWebview] do WebView.</span><span class="sxs-lookup"><span data-stu-id="29621-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="29621-129">Selecione seu destino desejado para anexar e abrir uma nova instância da guia do DevTools.</span><span class="sxs-lookup"><span data-stu-id="29621-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source=".//media/chooser_local.png" alt-text="Painel local do aplicativo DevTools":::
   <span data-ttu-id="29621-131">Painel local do aplicativo DevTools</span><span class="sxs-lookup"><span data-stu-id="29621-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="29621-132">Depuração remota</span><span class="sxs-lookup"><span data-stu-id="29621-132">Remote debugging</span></span>  

<span data-ttu-id="29621-133">O aplicativo Microsoft Edge DevTools introduz o suporte básico para depurar páginas em um computador remoto por meio do nosso novo [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="29621-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="29621-134">A versão mais recente vem com o acesso remoto à funcionalidade central no [Depurador][DevtoolsGuideEdgehtml|::ref10::|], nos[Elementos][DevtoolsGuideEdgehtml|::ref11::|] \(para operações somente leitura\) e nos painéis do[Console][DevtoolsGuideEdgehtml|::ref12::|].</span><span class="sxs-lookup"><span data-stu-id="29621-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="29621-135">O depurador remoto está limitado ao Microsoft Edge \(EdgeHTML\) executando hosts da área de trabalho, com suporte para outros hosts EdgeHTML e dispositivos com Windows 10 chegando nas versões futuras.</span><span class="sxs-lookup"><span data-stu-id="29621-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="29621-136">Para começar, confira a seção de documentos [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex]do[*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview].</span><span class="sxs-lookup"><span data-stu-id="29621-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./media/chooser_remote.png" alt-text="Painel remoto do aplicativo DevTools":::
   <span data-ttu-id="29621-138">Painel remoto do aplicativo DevTools</span><span class="sxs-lookup"><span data-stu-id="29621-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="29621-139">Atalhos gerais</span><span class="sxs-lookup"><span data-stu-id="29621-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="29621-140">Todos os atalhos foram verificados na versão mais recente do Windows.</span><span class="sxs-lookup"><span data-stu-id="29621-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="29621-141">Se não for possível usar um atalho, atualize sua cópia do Windows.</span><span class="sxs-lookup"><span data-stu-id="29621-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="29621-142">Esses atalhos controlam a janela principal do DevTools e devem funcionar em todas as ferramentas.</span><span class="sxs-lookup"><span data-stu-id="29621-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="29621-143">Ação</span><span class="sxs-lookup"><span data-stu-id="29621-143">Action</span></span> | <span data-ttu-id="29621-144">Atalho</span><span class="sxs-lookup"><span data-stu-id="29621-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="29621-145">Mostrar/Ocultar DevTools \(abre para o último painel exibido\)</span><span class="sxs-lookup"><span data-stu-id="29621-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="29621-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="29621-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="29621-147">Alternar encaixe \(Desencaixar/Abaixo/Direita\)</span><span class="sxs-lookup"><span data-stu-id="29621-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="29621-148">Abrir arquivo</span><span class="sxs-lookup"><span data-stu-id="29621-148">Open file</span></span> | `Ctrl`<span data-ttu-id="29621-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="29621-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="29621-150">Mostrar código-fonte HTML não editável no depurador</span><span class="sxs-lookup"><span data-stu-id="29621-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="29621-151">Mostrar/ocultar Console na parte inferior de qualquer outra ferramenta</span><span class="sxs-lookup"><span data-stu-id="29621-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="29621-152">Alternar para Elementos \(explorador do DOM\)</span><span class="sxs-lookup"><span data-stu-id="29621-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="29621-153">Alternar para Console</span><span class="sxs-lookup"><span data-stu-id="29621-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="29621-154">Alternar para Depurador</span><span class="sxs-lookup"><span data-stu-id="29621-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="29621-155">Alternar para Rede</span><span class="sxs-lookup"><span data-stu-id="29621-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="29621-156">Alternar para Desempenho</span><span class="sxs-lookup"><span data-stu-id="29621-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="29621-157">Alternar para Memória</span><span class="sxs-lookup"><span data-stu-id="29621-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="29621-158">Alternar para Emulação</span><span class="sxs-lookup"><span data-stu-id="29621-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="29621-159">Documento de Ajuda</span><span class="sxs-lookup"><span data-stu-id="29621-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="29621-160">Próxima ferramenta</span><span class="sxs-lookup"><span data-stu-id="29621-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="29621-161">Guia anterior</span><span class="sxs-lookup"><span data-stu-id="29621-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="29621-162">Ferramenta anterior \(do histórico\)</span><span class="sxs-lookup"><span data-stu-id="29621-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="29621-163">Próxima ferramenta \(do histórico\)</span><span class="sxs-lookup"><span data-stu-id="29621-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="29621-164">Próximo subquadro</span><span class="sxs-lookup"><span data-stu-id="29621-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="29621-165">Subquadro anterior</span><span class="sxs-lookup"><span data-stu-id="29621-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="29621-166">Próxima correspondência na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="29621-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="29621-167">Correspondência anterior na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="29621-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="29621-168">Procurar na caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="29621-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="29621-169">Focalizar o console na parte inferior</span><span class="sxs-lookup"><span data-stu-id="29621-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="29621-170">Iniciar o DevTools para o Console</span><span class="sxs-lookup"><span data-stu-id="29621-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="29621-171">Atualizar a página</span><span class="sxs-lookup"><span data-stu-id="29621-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="29621-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="29621-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="29621-173">Se você estiver depurando e pausar em um ponto de interrupção, a ação **Atualizar a página** retoma o tempo de execução primeiro.</span><span class="sxs-lookup"><span data-stu-id="29621-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="29621-174">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="29621-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="29621-175">Envie seus comentários para ajudar a melhorar o Microsoft Edge \ (EdgeHTML\) DevTools para você!</span><span class="sxs-lookup"><span data-stu-id="29621-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="29621-176">Basta abrir as ferramentas \(`F12`\) e selecionar o botão [Enviar comentários](#microsoft-edge-edgehtml-developer-tools).</span><span class="sxs-lookup"><span data-stu-id="29621-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="29621-177">Torne-se um Participante do Programa Windows Insider para visualizar os [recursos mais recentes que estão chegando à DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="29621-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="29621-178">Use o aplicativo Hub do Windows Feedback para publicar, votar, acompanhar e obter suporte para sugestões gerais e problemas do Windows.</span><span class="sxs-lookup"><span data-stu-id="29621-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Console"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulação"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Memória"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Rede"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Desempenho"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Profissionais de Serviço"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Armazenamento"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo de DevTools Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Visualização do Microsoft Edge DevTools - Clientes do Protocolo DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) para aplicativos do Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicativos de web progressivos (EdgeHTML) no Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Visualização do Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste gratuito do navegador Microsoft Edge | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  