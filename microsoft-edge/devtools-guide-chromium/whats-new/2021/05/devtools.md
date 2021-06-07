---
description: O botão Mais Ferramentas, documentação no contexto para começar a usar a extensão DevTools, maior suporte para leitores de tela no Console e muito mais.
title: Novidades no DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590837"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a><span data-ttu-id="e2547-104">Novidades no DevTools (Microsoft Edge 92)</span><span class="sxs-lookup"><span data-stu-id="e2547-104">What's New In DevTools (Microsoft Edge 92)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> <span data-ttu-id="e2547-105">A **conferência do Microsoft Build 2021** foi de 25 a 27 de maio.</span><span class="sxs-lookup"><span data-stu-id="e2547-105">The **Microsoft Build 2021** conference was on May 25-27.</span></span>  <span data-ttu-id="e2547-106">Veja um vídeo do Build sobre as atualizações para o DevTools: [Microsoft Edge | Estado da plataforma][YoutubeEdgeStateOfThePlatform] - Microsoft Edge uma plataforma atraente e consistente com ferramentas para desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="e2547-106">Here's a video from Build about the updates to DevTools: [Microsoft Edge | State of the Platform][YoutubeEdgeStateOfThePlatform] - Microsoft Edge brings a compelling and consistent platform with tools for developers.</span></span>  <span data-ttu-id="e2547-107">À medida que nossos navegadores herdados estão sem suporte, o Edge em breve será o único navegador com suporte da Microsoft no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2547-107">As our legacy browsers phase out of support, Edge will soon be the only supported browser from Microsoft on Windows 10.</span></span>  <span data-ttu-id="e2547-108">Junte-se a nós para saber mais sobre o mais recente na plataforma de Borda, ferramentas e aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="e2547-108">Join us to learn about the latest across the Edge platform, tools, and web apps.</span></span>


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a><span data-ttu-id="e2547-109">O botão Fechar não fica mais oculto quando o DevTools é estreito</span><span class="sxs-lookup"><span data-stu-id="e2547-109">The Close button is no longer hidden when DevTools is narrow</span></span>

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

<span data-ttu-id="e2547-110">Na Microsoft Edge versão 91 ou anterior, o botão Fechar para fechar DevTools não é exibido quando o visor DevTools é estreito. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e2547-110">In Microsoft Edge version 91 or earlier, the **Close** button to close DevTools isn't displayed when the DevTools viewport is narrow.</span></span>  <span data-ttu-id="e2547-111">Na Microsoft Edge versão 92, o botão **Fechar** no DevTools está sempre presente, independentemente da largura do viewport DevTools.</span><span class="sxs-lookup"><span data-stu-id="e2547-111">In Microsoft Edge version 92, the **Close** button in the DevTools is always present, regardless of the DevTools viewport width.</span></span>

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="O botão Fechar DevTools agora está presente mesmo quando o viewport é estreito" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   <span data-ttu-id="e2547-113">O **botão Fechar** DevTools agora está presente mesmo quando o viewport é estreito</span><span class="sxs-lookup"><span data-stu-id="e2547-113">The **Close** DevTools button is now present even when the viewport is narrow</span></span>  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a><span data-ttu-id="e2547-114">Adicionar ferramentas rapidamente com o novo botão Mais Ferramentas</span><span class="sxs-lookup"><span data-stu-id="e2547-114">Add tools quickly with the new More Tools button</span></span>

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

<span data-ttu-id="e2547-115">Há uma nova maneira de abrir mais ferramentas no Microsoft Edge DevTools: o menu **Mais Ferramentas** ( `+` ) .</span><span class="sxs-lookup"><span data-stu-id="e2547-115">There's a new way to open more tools in Microsoft Edge DevTools: the **More Tools** (`+`) menu.</span></span> <span data-ttu-id="e2547-116">O **menu Mais Ferramentas** aparece na barra de ferramentas no painel principal e na barra de ferramentas da gaveta.</span><span class="sxs-lookup"><span data-stu-id="e2547-116">The **More Tools** menu appears on the toolbar in the main panel and on the toolbar of the drawer.</span></span> <span data-ttu-id="e2547-117">Selecionar uma ferramenta no menu **Mais Ferramentas** adiciona a ferramenta à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e2547-117">Selecting a tool from the **More Tools** menu adds the tool to the toolbar.</span></span>

<span data-ttu-id="e2547-118">Para reordenar as guias em qualquer barra de ferramentas, selecione e arraste as guias.</span><span class="sxs-lookup"><span data-stu-id="e2547-118">To reorder the tabs on either toolbar, select and drag the tabs.</span></span>  

<span data-ttu-id="e2547-119">O **menu Mais Ferramentas** estava disponível como um experimento na Microsoft Edge versão 89 e agora está sempre presente.</span><span class="sxs-lookup"><span data-stu-id="e2547-119">The **More Tools** menu was available as an experiment in Microsoft Edge version 89, and is now always present.</span></span>

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="O botão Mais Ferramentas na barra de ferramentas superior e na barra de ferramentas da gaveta" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   <span data-ttu-id="e2547-121">O **botão Mais Ferramentas** na barra de ferramentas superior e na barra de ferramentas da gaveta</span><span class="sxs-lookup"><span data-stu-id="e2547-121">The **More Tools** button on the upper toolbar and drawer toolbar</span></span>
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="O menu Mais Ferramentas" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   <span data-ttu-id="e2547-123">O menu **Mais Ferramentas**</span><span class="sxs-lookup"><span data-stu-id="e2547-123">The **More Tools** menu</span></span>
:::image-end:::  


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a><span data-ttu-id="e2547-124">Melhorias para ferramentas de foco, seleção e fechamento</span><span class="sxs-lookup"><span data-stu-id="e2547-124">Improvements for hovering, selecting, and closing tools</span></span>

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

<span data-ttu-id="e2547-125">Guias para cada ferramenta foram reformatados para reduzir a chance de fechar acidentalmente uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="e2547-125">Tabs for each tool have been reformatted to reduce the chance of accidentally closing a tool.</span></span>  <span data-ttu-id="e2547-126">Em cada guia na barra de ferramentas principal e na barra de ferramentas da gaveta, adicionamos:</span><span class="sxs-lookup"><span data-stu-id="e2547-126">On each tab in the main toolbar and in the toolbar of the drawer, we added:</span></span>
*  <span data-ttu-id="e2547-127">Espaçamento ao redor da guia.</span><span class="sxs-lookup"><span data-stu-id="e2547-127">Spacing around the tab.</span></span>
*  <span data-ttu-id="e2547-128">Espaçamento ao redor do botão fechar ( `x` ) na guia.</span><span class="sxs-lookup"><span data-stu-id="e2547-128">Spacing around the close (`x`) button in the tab.</span></span>
*  <span data-ttu-id="e2547-129">Uma cor de plano de fundo ao passar o mouse sobre a guia.</span><span class="sxs-lookup"><span data-stu-id="e2547-129">A background color when hovering over the tab.</span></span>
*  <span data-ttu-id="e2547-130">Uma dica de ferramenta para o botão fechar ( `x` ) da guia.</span><span class="sxs-lookup"><span data-stu-id="e2547-130">A tooltip for the close (`x`) button of the tab.</span></span>
*  <span data-ttu-id="e2547-131">Contraste mais alto para o botão fechar ( `x` ) da guia.</span><span class="sxs-lookup"><span data-stu-id="e2547-131">Higher contrast for the close (`x`) button of the tab.</span></span>

<span data-ttu-id="e2547-132">Por exemplo, quando você estiver na ferramenta \*\*\*\* **Desempenho** e passar o mouse sobre a guia da ferramenta Rede, essas melhorias ajudam a impedir o fechamento acidental **da ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="e2547-132">For example, when you are in the **Performance** tool and you hover over the **Network** tool's tab, these improvements help prevent accidentally closing the **Network** tool.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Guias antes da reformatação" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           <span data-ttu-id="e2547-134">Guias antes da reformatação</span><span class="sxs-lookup"><span data-stu-id="e2547-134">Tabs before reformatting</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Guias após a reformatação" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           <span data-ttu-id="e2547-136">Guias após a reformatação</span><span class="sxs-lookup"><span data-stu-id="e2547-136">Tabs after reformatting</span></span> :::image-end:::
    :::column-end:::
:::row-end:::

<span data-ttu-id="e2547-137">Essas melhorias são especialmente relevantes para os usuários do DevTools localizado, no qual as guias podem ser mais estreitas e mais fáceis de fechar acidentalmente.</span><span class="sxs-lookup"><span data-stu-id="e2547-137">These improvements are especially relevant for users of localized DevTools, in which the tabs may be narrower and easier to accidentally close.</span></span>

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="DevTools localizado com guias estreitas" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   <span data-ttu-id="e2547-139">DevTools localizado com guias estreitas</span><span class="sxs-lookup"><span data-stu-id="e2547-139">Localized DevTools with narrow tabs</span></span>
:::image-end:::

<span data-ttu-id="e2547-140">Também facilitamos a nova adição de uma ferramenta que você fechou adicionando um [menu](#add-tools-quickly-with-the-new-more-tools-button) Mais Ferramentas à barra de ferramentas principal e à barra de ferramentas da gaveta.</span><span class="sxs-lookup"><span data-stu-id="e2547-140">We also made it easier to re-add a tool that you closed by adding a [More Tools menu](#add-tools-quickly-with-the-new-more-tools-button) to the main toolbar and drawer toolbar.</span></span>


## <a name="better-support-for-screen-readers-in-the-console"></a><span data-ttu-id="e2547-141">Melhor suporte para leitores de tela no Console</span><span class="sxs-lookup"><span data-stu-id="e2547-141">Better support for screen readers in the Console</span></span>

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

<span data-ttu-id="e2547-142">Antes da Microsoft Edge versão 92, no **Console,** as tecnologias assistivas, como leitores de tela, não anunciam sugestões de preenchimento automático ou os resultados das expressões avaliadas.</span><span class="sxs-lookup"><span data-stu-id="e2547-142">Prior to Microsoft Edge version 92, in the **Console**, assistive technologies such as screen readers didn't announce autocomplete suggestions or the results of evaluated expressions.</span></span> <span data-ttu-id="e2547-143">Isso foi corrigido agora.</span><span class="sxs-lookup"><span data-stu-id="e2547-143">This has been fixed now.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="No Console, os leitores de tela agora anunciam a sugestão de preenchimento automático selecionado no momento" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           <span data-ttu-id="e2547-145">No **Console ,** os leitores de tela agora anunciam a sugestão de preenchimento automático selecionado no momento</span><span class="sxs-lookup"><span data-stu-id="e2547-145">In the **Console**, screen readers now announce the currently selected autocomplete suggestion</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="No Console, os leitores de tela agora anunciam o resultado de uma expressão avaliada" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           <span data-ttu-id="e2547-147">No **Console ,** os leitores de tela agora anunciam o resultado de uma expressão avaliada</span><span class="sxs-lookup"><span data-stu-id="e2547-147">In the **Console**, screen readers now announce the result of an evaluated expression</span></span> :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a><span data-ttu-id="e2547-148">Microsoft Edge Ferramentas de desenvolvedor Visual Studio Code versão 1.1.8</span><span class="sxs-lookup"><span data-stu-id="e2547-148">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.8</span></span>

<span data-ttu-id="e2547-149">O [Microsoft Edge ferramentas][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de desenvolvedor para Visual Studio Code versão 1.1.8 do Microsoft Visual Studio Code tem as seguintes alterações desde a versão anterior.</span><span class="sxs-lookup"><span data-stu-id="e2547-149">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="e2547-150">O Microsoft Visual Studio Code atualiza as extensões automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e2547-150">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="e2547-151">Para atualizar manualmente para a versão 1.1.8, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="e2547-151">To manually update to version 1.1.8, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

<span data-ttu-id="e2547-152">Você pode registrar problemas e contribuir para a extensão no [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="e2547-152">You can file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a><span data-ttu-id="e2547-153">Documentação no contexto e interface do usuário para facilitar o uso da extensão DevTools</span><span class="sxs-lookup"><span data-stu-id="e2547-153">In-context documentation and UI to make it easier to use the DevTools extension</span></span>

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

<span data-ttu-id="e2547-154">A versão 1.1.8 do Microsoft Edge [Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension agora apresenta uma maneira mais simples de iniciar uma nova instância do Microsoft Edge, apresentando instruções, botões, links e uma página de documentação para orientá-lo.</span><span class="sxs-lookup"><span data-stu-id="e2547-154">Version 1.1.8 of the [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension now features a simpler way to start a new instance of Microsoft Edge, by presenting instructions, buttons, links, and a documentation page to guide you.</span></span>

*  <span data-ttu-id="e2547-155">Quando você seleciona o botão **ferramentas** \*\*\*\* Microsoft Edge na Barra de Atividades do Visual Studio Code, o painel Ferramentas **Microsoft Edge: Destinos** agora apresenta texto explicativo, botões e links para orientá-lo, em vez de um painel em branco.</span><span class="sxs-lookup"><span data-stu-id="e2547-155">When you select the **Microsoft Edge Tools** button in the **Activity Bar** of Visual Studio Code, the **Microsoft Edge Tools: Targets** panel now presents explanatory text, buttons, and links to guide you, instead of a blank panel.</span></span>

*  <span data-ttu-id="e2547-156">Quando você abre uma nova instância de Microsoft Edge de dentro do Visual Studio Code, o Microsoft Edge agora mostra uma página inicial que explica como usar a extensão Ferramentas do Desenvolvedor, em vez de uma página em branco.</span><span class="sxs-lookup"><span data-stu-id="e2547-156">When you open a new instance of Microsoft Edge from within Visual Studio Code, Microsoft Edge now shows a start page that explains how to use the Developer Tools extension, instead of a blank page.</span></span>

*  <span data-ttu-id="e2547-157">O **Microsoft Edge Ferramentas: Destinos** agora tem um botão **Gerar** launch.jsno botão e instruções, para ajudar a iniciar seu projeto para depuração em Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e2547-157">The **Microsoft Edge Tools: Targets** panel now has a **Generate launch.json** button and instructions, to help launch your project for debugging in Microsoft Edge.</span></span>

<span data-ttu-id="e2547-158">Para obter mais informações, navegue [até Usando as ferramentas][GithubIoDevToolsUsing].</span><span class="sxs-lookup"><span data-stu-id="e2547-158">For more information, navigate to [Using the tools][GithubIoDevToolsUsing].</span></span>


## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="e2547-159">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e2547-159">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="e2547-160">Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="e2547-160">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="e2547-161">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="e2547-161">The preview channels give you access to the latest DevTools features.</span></span>  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="e2547-162">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e2547-162">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Usando as ferramentas | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace de Extensões | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Ferramentas de desenvolvedor para Visual Studio Code | Visual Studio Marketplace"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: estado da plataforma | YouTube"

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e2547-170">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2547-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
