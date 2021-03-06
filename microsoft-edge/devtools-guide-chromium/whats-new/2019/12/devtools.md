---
description: Melhorias de acessibilidade, uso do DevTools em outros idiomas e muito mais.
title: Novidades no DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 80f870d22c81479bff9b9413717ccc7c323d9a05
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397556"
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

# <a name="whats-new-in-devtools-microsoft-edge-80"></a><span data-ttu-id="895af-104">Novidades no DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="895af-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="895af-105">Comunicados da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="895af-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="895af-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="895af-107">Confira os comunicados para experimentar novos recursos no DevTools, no Microsoft Visual Studio Code e muito mais.</span><span class="sxs-lookup"><span data-stu-id="895af-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="895af-108">Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="895af-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="895af-109">Melhorias de acessibilidade no DevTools</span><span class="sxs-lookup"><span data-stu-id="895af-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="895af-110">A equipe do DevTools contribuiu com 170 alterações no Chromium para resolver problemas de contraste de cores de alto impacto, teclado e leitor de tela no DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="895af-111">Cada desenvolvedor que está criando a Web deve ser capaz de usar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="A ferramenta Performance no DevTools com as melhorias de navegação de teclado e leitor de tela" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="895af-113">A **ferramenta Performance** no DevTools com as melhorias de navegação de teclado e leitor de tela</span><span class="sxs-lookup"><span data-stu-id="895af-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="895af-114">Quer saber como tornar sua página da Web acessível para todos os usuários?</span><span class="sxs-lookup"><span data-stu-id="895af-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="895af-115">Baixe as [Percepções de Acessibilidade][AccessibilityInsights] [e extensões webhint][WebhintBrowserExtension] do Microsoft Edge para começar.</span><span class="sxs-lookup"><span data-stu-id="895af-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="895af-116">Se você usar leitores de tela ou o teclado para navegar [][PostTweetEdgeDevTools] ao redor do DevTools, envie seus comentários tuitando para nós ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="895af-116">If you use screen readers or the keyboard to navigate around the DevTools, send your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="895af-117">Problema do Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="895af-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="895af-118">Usando o DevTools em outros idiomas</span><span class="sxs-lookup"><span data-stu-id="895af-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="895af-119">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code, em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="895af-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="895af-120">Estamos animados para anunciar a localização para o DevTools, que agora você pode usar em um dos 10 idiomas além do inglês:</span><span class="sxs-lookup"><span data-stu-id="895af-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="895af-121">Chinês \(Simplificado\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="895af-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="895af-122">Chinês \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="895af-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="895af-123">Francês –&#231;ais</span><span class="sxs-lookup"><span data-stu-id="895af-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="895af-124">Alemão - deutsch</span><span class="sxs-lookup"><span data-stu-id="895af-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="895af-125">Italiano - italiano</span><span class="sxs-lookup"><span data-stu-id="895af-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="895af-126">Japonês - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="895af-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="895af-127">Coreano - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="895af-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="895af-128">Português - portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="895af-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="895af-129">Russo – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="895af-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="895af-130">Espanhol - espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="895af-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="895af-131">Navegue `edge://flags` até e de definir o sinalizador **Habilitar ferramentas de desenvolvedor localizadas** **como Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="895af-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="895af-132">Também de definir o **sinalizador de experimentos de Ferramentas de** Desenvolvedor como **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="895af-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="895af-133">Reinicie o Microsoft Edge e abra o DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="895af-134">Os DevTools combinam com o idioma que você usa para o Microsoft Edge em `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="895af-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   <span data-ttu-id="895af-136">O DevTools em alemão</span><span class="sxs-lookup"><span data-stu-id="895af-136">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="895af-137">Se você quiser usar o DevTools em um idioma diferente dos que estão disponíveis, [tweet][PostTweetEdgeDevTools] para nós ou escolha o [ícone Enviar Comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="895af-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="895af-138">Problema do Chromium [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="895af-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="895af-139">extensão webhint do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="895af-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="895af-140">A extensão webhint do Microsoft Edge permite que você digitalizar facilmente sua página da Web e obter comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="895af-141">Leia mais em [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="895af-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="A ferramenta Hints no DevTools quando a extensão do navegador webhint é instalada" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   <span data-ttu-id="895af-143">A **ferramenta Hints** no DevTools quando a extensão do navegador webhint é instalada</span><span class="sxs-lookup"><span data-stu-id="895af-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="895af-144">[Experimente a extensão do navegador webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="895af-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="895af-145">Depois de instalar a extensão, abra o DevTools e escolha a **ferramenta Dicas.**</span><span class="sxs-lookup"><span data-stu-id="895af-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="895af-146">A partir daqui, execute uma verificação de site personalizável.</span><span class="sxs-lookup"><span data-stu-id="895af-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="895af-147">Vá até [webhint.io][WebhintBrowserExtension] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="895af-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <a name="3d-view"></a><span data-ttu-id="895af-148">Modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="895af-148">3D View</span></span>  

<span data-ttu-id="895af-149">Use o **View 3D** para depurar seu aplicativo Web navegando pelo modelo de objeto de documento [\(DOM\)][MDNDocumentObjectModel] ou o contexto de empilhamento [de índice z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="895af-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="A exibição 3D no DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   <span data-ttu-id="895af-151">A **exibição 3D** no DevTools</span><span class="sxs-lookup"><span data-stu-id="895af-151">The **3D View** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="895af-152">Para acessar o Modo de Exibição 3D, navegue até e verifique se o sinalizador de experimentos de Ferramentas de Desenvolvedor está `edge://flags` definido como **Habilitado**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="895af-152">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="895af-153">Reinicie o Microsoft Edge e abra o DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-153">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="895af-154">Selecione na seção DevTools ou abra a seção Experimentos de Configurações e ative a caixa de seleção Habilitar o Modo de `F1` \*\*\*\*  >  \*\*\*\* Exibição **3D.**</span><span class="sxs-lookup"><span data-stu-id="895af-154">Select `F1` in the DevTools or open the **Settings** > **Experiments** section, and turn on the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="895af-155">Agora, selecione `Ctrl`  +  `Shift`  +  `P` , digite em **Exibição 3D** e selecione **Mostrar Exibição 3D**.</span><span class="sxs-lookup"><span data-stu-id="895af-155">Now, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="895af-156">Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao Modo de Exibição 3D, portanto, envie seus [comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="895af-156">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="895af-157">Problema do Chromium [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="895af-157">Chromium issue [#987787][CR987787]</span></span>

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="895af-158">Visual Studio extensões de código</span><span class="sxs-lookup"><span data-stu-id="895af-158">Visual Studio Code extensions</span></span>  

<span data-ttu-id="895af-159">A equipe do DevTools também lançou algumas extensões para Visual Studio [Code][VisualStudioCode] que permitem que você use o poder do DevTools diretamente do seu editor de texto.</span><span class="sxs-lookup"><span data-stu-id="895af-159">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor.</span></span> <span data-ttu-id="895af-160">Confira as seguintes extensões.</span><span class="sxs-lookup"><span data-stu-id="895af-160">Check out the following extensions.</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="895af-161">Elementos para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="895af-161">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="895af-162">Use a ferramenta Elements de dentro Visual Studio Code adicionando a extensão [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="895af-162">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="A ferramenta Elements no Visual Studio Code usando a extensão Elements for Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   <span data-ttu-id="895af-164">A **ferramenta Elements** no Visual Studio Code usando a extensão Elements for Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="895af-164">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="895af-165">Para obter mais informações, confira [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="895af-165">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="895af-166">Depurador para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="895af-166">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="895af-167">Com a [extensão Depurador do Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depure JavaScript em execução no Microsoft Edge diretamente do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="895af-167">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="O Depurador para a Extensão do Microsoft Edge em Visual Studio Código" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   <span data-ttu-id="895af-169">O Depurador para a Extensão do Microsoft Edge em Visual Studio Código</span><span class="sxs-lookup"><span data-stu-id="895af-169">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="895af-170">Para obter mais informações, confira [como depurar o Microsoft Edge de Visual Studio Código][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="895af-170">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="895af-171">Dica da web</span><span class="sxs-lookup"><span data-stu-id="895af-171">webhint</span></span>  

<span data-ttu-id="895af-172">A [extensão webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code usa `webhint` para melhorar sua página da Web enquanto você a escreve!</span><span class="sxs-lookup"><span data-stu-id="895af-172">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="895af-173">Essa extensão é executado e relata diagnósticos em seus arquivos de espaço de trabalho com base na `webhint` análise.</span><span class="sxs-lookup"><span data-stu-id="895af-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="A extensão webhint Visual Studio Code analisando um arquivo .tsx em Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="895af-175">A extensão webhint Visual Studio Code analisando um `.tsx` arquivo em Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="895af-175">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="895af-176">[Saiba mais sobre a extensão webhint Visual Studio Code][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="895af-176">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="895af-177">Visual Studio integração</span><span class="sxs-lookup"><span data-stu-id="895af-177">Visual Studio integration</span></span>  

<span data-ttu-id="895af-178">No Visual Studio 2019 versão 16.2 ou posterior, use o depurador Visual Studio para depurar JavaScript em execução no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="895af-178">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="895af-179">[Baixe Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="895af-179">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out.</span></span>  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2019/12/vs.msft.png":::
   <span data-ttu-id="895af-181">Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canary, Dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="895af-181">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="895af-182">[Leia nossa postagem de blog para saber como depurar o Microsoft Edge Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="895af-182">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="895af-183">Acompanhamento de mensagens de console de prevenção</span><span class="sxs-lookup"><span data-stu-id="895af-183">Tracking prevention Console messages</span></span>  

<span data-ttu-id="895af-184">A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que impede que você seja rastreado por um site antes de visitá-lo.</span><span class="sxs-lookup"><span data-stu-id="895af-184">Tracking prevention is a unique feature in Microsoft Edge that blocks you from being tracked by a website before you visited it.</span></span>  <span data-ttu-id="895af-185">A configuração de prevenção de rastreamento padrão é o modo Balanceado, que bloqueia rastreadores de terceiros e rastreadores mal-intencionados conhecidos para uma experiência que equilibra a privacidade e a compatibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="895af-185">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="895af-186">Para dar mais informações sobre a compatibilidade da página da Web quando determinados rastreadores são bloqueados, a equipe do Microsoft Edge adicionou mensagens de aviso no **Console** quando um rastreador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="895af-186">To give you more insight into the compatibility of your web page when certain trackers are blocked, The Microsoft Edge team added warning messages in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Mensagens no Console quando o controle de prevenção bloqueia o acesso ao armazenamento de um rastreador" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   <span data-ttu-id="895af-188">Mensagens no **Console quando o controle** de prevenção bloqueia o acesso ao armazenamento de um rastreador</span><span class="sxs-lookup"><span data-stu-id="895af-188">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="895af-189">[Leia mais sobre como controlar a prevenção e o equilíbrio entre privacidade e compatibilidade com a Web.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="895af-189">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="895af-190">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="895af-190">Announcements from the Chromium project</span></span>  

<span data-ttu-id="895af-191">As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 80 que contribuíram para o projeto Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="895af-191">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a><span data-ttu-id="895af-192">Suporte para redesclarações de let e class no Console</span><span class="sxs-lookup"><span data-stu-id="895af-192">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="895af-193">O **Console** agora dá suporte a reclarações `let` de e `class` instruções.</span><span class="sxs-lookup"><span data-stu-id="895af-193">The **Console** now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="895af-194">A incapacidade de redeclarar era um aborrecimento comum para desenvolvedores da Web que usam o Console para experimentar com o novo código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="895af-194">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="895af-195">Redeclar uma instrução ou em um script fora do Console ou dentro de uma `let` única entrada do Console ainda causa um `class` `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="895af-195">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="895af-196">Por exemplo, anteriormente, ao declarar uma variável local com `let` , o Console lançou um erro:</span><span class="sxs-lookup"><span data-stu-id="895af-196">For example, previously, when re-declaring a local variable with `let`, the Console threw an error:</span></span>  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="O Console no Microsoft Edge 79 mostrando que a redeclaração permitir falha" lightbox="../../images/2019/12/letbefore.msft.png":::
   <span data-ttu-id="895af-198">O **Console** no Microsoft Edge 79 mostrando que a declaração permitir falha</span><span class="sxs-lookup"><span data-stu-id="895af-198">The **Console** in Microsoft Edge 79 showing that the let re-declaration fails</span></span>  
:::image-end:::  

<span data-ttu-id="895af-199">Agora, o Console permite a reclaração:</span><span class="sxs-lookup"><span data-stu-id="895af-199">Now, the Console allows the redeclaration:</span></span>  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="O Console no Microsoft Edge 80 mostrando que a redeclaração de permitir é bem-sucedida" lightbox="../../images/2019/12/letafter.msft.png":::
   <span data-ttu-id="895af-201">O **Console** no Microsoft Edge 80 mostrando que a re-declaração let é bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="895af-201">The **Console** in Microsoft Edge 80 showing that the let re-declaration succeeds</span></span>  
:::image-end:::  

<span data-ttu-id="895af-202">Problema do Chromium [#1004193][CR1004193]</span><span class="sxs-lookup"><span data-stu-id="895af-202">Chromium issue [#1004193][CR1004193]</span></span>  

### <a name="improved-webassembly-debugging"></a><span data-ttu-id="895af-203">Depuração webAssembly aprimorada</span><span class="sxs-lookup"><span data-stu-id="895af-203">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="895af-204">O DevTools começou a dar suporte ao PADRÃO DE [Depuração ANÃO][DwarfHome], o que significa maior suporte para passar o código, definir pontos de interrupção e resolver rastreamentos de pilha em seus idiomas de origem no DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-204">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a><span data-ttu-id="895af-205">Atualizações do painel de rede</span><span class="sxs-lookup"><span data-stu-id="895af-205">Network panel updates</span></span>  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a><span data-ttu-id="895af-206">Solicitar cadeias de iniciadores no painel Iniciador</span><span class="sxs-lookup"><span data-stu-id="895af-206">Request Initiator Chains in the Initiator panel</span></span>  

<span data-ttu-id="895af-207">Agora você pode exibir os iniciadores e dependências de uma solicitação de rede como uma lista aninhada.</span><span class="sxs-lookup"><span data-stu-id="895af-207">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="895af-208">Isso pode ajudá-lo a entender por que um recurso foi solicitado ou qual atividade de rede um determinado recurso \(como um script\) causou.</span><span class="sxs-lookup"><span data-stu-id="895af-208">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Uma cadeia de iniciador de solicitação no painel Iniciador" lightbox="../../images/2019/12/initiators.msft.png":::
   <span data-ttu-id="895af-210">Uma cadeia de iniciador de solicitação no painel **Iniciador**</span><span class="sxs-lookup"><span data-stu-id="895af-210">A Request Initiator Chain in the **Initiator** panel</span></span>  
:::image-end:::  

<span data-ttu-id="895af-211">Depois [de registrar atividade de rede][DevToolsNetworkIndex]no painel Rede, escolha um recurso e navegue até o painel **Iniciador** para exibir a **Cadeia de Iniciador de Solicitação**:</span><span class="sxs-lookup"><span data-stu-id="895af-211">After [logging network activity in the Network panel][DevToolsNetworkIndex], choose a resource and then navigate to the **Initiator** panel to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="895af-212">O **recurso inspecionado** é negrito.</span><span class="sxs-lookup"><span data-stu-id="895af-212">The **inspected resource** is bold.</span></span>  <span data-ttu-id="895af-213">Na captura de tela acima, `ai.2.min.js` está o recurso inspecionado.</span><span class="sxs-lookup"><span data-stu-id="895af-213">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="895af-214">Os recursos acima do recurso inspecionado são os **iniciadores**.</span><span class="sxs-lookup"><span data-stu-id="895af-214">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="895af-215">Na captura de tela acima, `https://www.microsoftedgeinsider.com` é o iniciador de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="895af-215">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="895af-216">Em outras palavras, `https://www.microsoftedgeinsider.com` causou a solicitação de rede para `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="895af-216">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="895af-217">Os recursos abaixo do recurso inspecionado são **as dependências**.</span><span class="sxs-lookup"><span data-stu-id="895af-217">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="895af-218">Na captura de tela acima, `https://dc.services.visualstudio.com/v2/track` há uma dependência de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="895af-218">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="895af-219">Em outras palavras, `ai.2.min.js` causou a solicitação de rede para `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="895af-219">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="895af-220">As informações de inicializador e dependência também podem ser acessadas segurando `Shift` e, em seguida, pairando sobre os recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="895af-220">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="895af-221">Navegue [até Exibir iniciadores e dependências.][DevToolsNetworkReferenceViewInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="895af-221">Navigate to [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="895af-222">Problema do Chromium [#842488][CR842488]</span><span class="sxs-lookup"><span data-stu-id="895af-222">Chromium issue [#842488][CR842488]</span></span>  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a><span data-ttu-id="895af-223">Realça a solicitação de rede selecionada na Visão Geral</span><span class="sxs-lookup"><span data-stu-id="895af-223">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="895af-224">Depois de escolher um recurso de rede para inspecioná-lo, o painel Rede agora coloca uma borda azul ao redor desse recurso na Visão **Geral**.</span><span class="sxs-lookup"><span data-stu-id="895af-224">After you choose a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="895af-225">Isso pode ajudá-lo a detectar se a solicitação de rede está ocorrendo antes ou mais tarde do que o esperado.</span><span class="sxs-lookup"><span data-stu-id="895af-225">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="O painel Visão Geral realçando o recurso inspecionado" lightbox="../../images/2019/12/overview.msft.png":::
   <span data-ttu-id="895af-227">O **painel Visão** Geral realçando o recurso inspecionado</span><span class="sxs-lookup"><span data-stu-id="895af-227">The **Overview** pane highlighting the inspected resource</span></span>  
:::image-end:::  

<span data-ttu-id="895af-228">Problema do Chromium [#988253][CR988253]</span><span class="sxs-lookup"><span data-stu-id="895af-228">Chromium issue [#988253][CR988253]</span></span>  

#### <a name="url-and-path-columns-in-the-network-panel"></a><span data-ttu-id="895af-229">Colunas de URL e caminho no painel Rede</span><span class="sxs-lookup"><span data-stu-id="895af-229">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="895af-230">Use as novas **colunas Path** e **URL** na ferramenta **Rede** para exibir o caminho absoluto ou a URL completa de cada recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="895af-230">Use the new **Path** and **URL** columns in the **Network** tool to display the absolute path or full URL of each network resource.</span></span>  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="As novas colunas Caminho e URL no painel Rede" lightbox="../../images/2019/12/columns.msft.png":::
   <span data-ttu-id="895af-232">As novas colunas Caminho e URL na **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="895af-232">The new Path and URL columns in the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="895af-233">Para exibir as novas colunas, passe o mouse no header da tabela **Cascata,** abra o menu contextual \(righ-click\) e escolha **Caminho** ou **URL**.</span><span class="sxs-lookup"><span data-stu-id="895af-233">To display the new columns, hover on the **Waterfall** table header, open the contextual menu \(righ-click\), and choose **Path** or **URL**.</span></span>  

<span data-ttu-id="895af-234">Problema do Chromium [#993366][CR993366]</span><span class="sxs-lookup"><span data-stu-id="895af-234">Chromium issue [#993366][CR993366]</span></span>  

#### <a name="updated-user-agent-strings"></a><span data-ttu-id="895af-235">Cadeias User-Agent cadeias de caracteres atualizadas</span><span class="sxs-lookup"><span data-stu-id="895af-235">Updated User-Agent strings</span></span>  

<span data-ttu-id="895af-236">O DevTools dá suporte à configuração de uma cadeia User-Agent de caracteres personalizada por meio do **painel Condições de** Rede.</span><span class="sxs-lookup"><span data-stu-id="895af-236">DevTools supports setting a custom User-Agent string through the **Network Conditions** panel.</span></span>  <span data-ttu-id="895af-237">A User-Agent de caracteres afeta o cabeçalho HTTP anexado aos recursos de rede e também `User-Agent` o valor de `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="895af-237">The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="895af-238">As cadeias de caracteres User-Agent foram atualizadas para refletir versões modernas do navegador.</span><span class="sxs-lookup"><span data-stu-id="895af-238">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="O menu Agente do Usuário no painel Condições de Rede" lightbox="../../images/2019/12/useragent.msft.png":::
   <span data-ttu-id="895af-240">O menu Agente do Usuário no painel **Condições de** Rede</span><span class="sxs-lookup"><span data-stu-id="895af-240">The User Agent menu in the **Network Conditions** panel</span></span>  
:::image-end:::  

<span data-ttu-id="895af-241">Para acessar **As Condições de Rede,** [abra o Menu de Comando][DevToolsCommandMenuIndex] e execute o `Show Network Conditions` comando.</span><span class="sxs-lookup"><span data-stu-id="895af-241">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="895af-242">Você também pode [definir User-Agent cadeias de caracteres no Modo de Dispositivo][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="895af-242">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="895af-243">Problema do Chromium [#1029031][CR1029031]</span><span class="sxs-lookup"><span data-stu-id="895af-243">Chromium issue [#1029031][CR1029031]</span></span>  

### <a name="audits-panel-updates"></a><span data-ttu-id="895af-244">Atualizações do painel de auditorias</span><span class="sxs-lookup"><span data-stu-id="895af-244">Audits panel updates</span></span>  

#### <a name="new-configuration-ui"></a><span data-ttu-id="895af-245">Nova interface do usuário de configuração</span><span class="sxs-lookup"><span data-stu-id="895af-245">New configuration UI</span></span>  

<span data-ttu-id="895af-246">A interface do usuário de configuração tem um design novo e responsivo e as opções de configuração de otimização foram simplificadas.</span><span class="sxs-lookup"><span data-stu-id="895af-246">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="895af-247">Para obter mais informações sobre as alterações na interface do usuário de throttling, navegue até [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span><span class="sxs-lookup"><span data-stu-id="895af-247">For more information on the throttling UI changes, navigate to [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span></span>  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="A nova interface do usuário de configuração" lightbox="../../images/2019/12/start.msft.png":::
   <span data-ttu-id="895af-249">A nova interface do usuário de configuração</span><span class="sxs-lookup"><span data-stu-id="895af-249">The new configuration UI</span></span>  
:::image-end:::  

### <a name="coverage-tool-updates"></a><span data-ttu-id="895af-250">Atualizações da ferramenta de cobertura</span><span class="sxs-lookup"><span data-stu-id="895af-250">Coverage tool updates</span></span>  

#### <a name="per-function-or-per-block-coverage-modes"></a><span data-ttu-id="895af-251">Modos de cobertura por função ou por bloco</span><span class="sxs-lookup"><span data-stu-id="895af-251">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="895af-252">A [ferramenta Coverage][DevToolsCoverageIndex] tem um novo menu suspenso que permite especificar se os dados de cobertura de código devem ser coletados por **função** ou **por bloco.**</span><span class="sxs-lookup"><span data-stu-id="895af-252">The [Coverage][DevToolsCoverageIndex] tool has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="895af-253">**A cobertura por** bloco é mais detalhada, mas também muito mais cara a ser cobrada.</span><span class="sxs-lookup"><span data-stu-id="895af-253">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="895af-254">O DevTools usa **por** padrão a cobertura por função.</span><span class="sxs-lookup"><span data-stu-id="895af-254">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="895af-255">Você pode notar grandes diferenças de cobertura de código em arquivos HTML, dependendo se você usa **por função** ou por **modo de** bloqueio.</span><span class="sxs-lookup"><span data-stu-id="895af-255">You may notice large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="895af-256">Ao usar **por modo de** função, scripts em linha em arquivos HTML são tratados como funções.</span><span class="sxs-lookup"><span data-stu-id="895af-256">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="895af-257">Se o script for executado, o DevTools marcará todo o script como código usado.</span><span class="sxs-lookup"><span data-stu-id="895af-257">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="895af-258">Somente se o script não for executado, o DevTools marcará o script como código nãoutilizado.</span><span class="sxs-lookup"><span data-stu-id="895af-258">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="O menu suspenso do modo de cobertura" lightbox="../../images/2019/12/modes.msft.png":::
   <span data-ttu-id="895af-260">O menu suspenso do modo de cobertura</span><span class="sxs-lookup"><span data-stu-id="895af-260">The coverage mode dropdown menu</span></span>  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a><span data-ttu-id="895af-261">A cobertura agora deve ser iniciada por uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="895af-261">Coverage must now be initiated by a page refresh</span></span>  

<span data-ttu-id="895af-262">A cobertura de código de agregação sem uma atualização de página foi removida porque os dados de cobertura não eram confiáveis.</span><span class="sxs-lookup"><span data-stu-id="895af-262">Toggling code coverage without a page refresh has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="895af-263">Por exemplo, uma função pode ser relatada como não usada se o tempo de execução foi há muito tempo e o coletor de lixo V8 a limpou.</span><span class="sxs-lookup"><span data-stu-id="895af-263">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="895af-264">Problema do Chromium [#1004203][CR1004203]</span><span class="sxs-lookup"><span data-stu-id="895af-264">Chromium issue [#1004203][CR1004203]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="895af-265">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="895af-265">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="895af-266">Se você estiver no Windows ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="895af-266">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="895af-267">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="895af-267">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="895af-268">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="895af-268">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Execute comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Encontre código JavaScript e CSS nãoutilado com a ferramenta Coverage no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular um modo de exibição móvel - Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Exibir iniciadores e dependências - Referência de Análise de Rede | Microsoft Docs"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Novidades no EdgeHTML | Microsoft Docs"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para o Microsoft Edge Visual Studio Extensão de código | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos para a extensão Visual Studio código do Microsoft Edge | Microsoft Docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Adicione o campo Iniciador à guia Headers | Bugs de cromo"  
[CR988253]: https://crbug.com/988253 "Bug DevTools - Nenhuma associação entre a solicitação de rede e o gráfico de linha do tempo | Bugs de cromo"  
[CR993366]: https://crbug.com/993366 "Mostre parte do caminho da URL na lista de solicitações do painel de rede | Bugs de cromo"  
[CR1004193]: https://crbug.com/1004193 "Modo REPL para V8 | Bugs de cromo"  
[CR1004203]: https://crbug.com/1004203 "Tornar a Cobertura de Código incrível | Bugs de cromo"  
[CR1029031]: https://crbug.com/1029031 "Cadeias de caracteres da UA estão ficando desatualizadas | Bugs de cromo" 
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Bugs de cromo"
[CR941561]: https://crbug.com/941561 "Localizabilidade do devTools | Bugs de cromo"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Bugs de cromo"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Percepções de acessibilidade"  

[DwarfHome]: https://dwarfstd.org "Casa anã"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Throttling do Painel de Auditorias do DevTools - GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema - MicrosoftDocs/desenvolvedor de borda"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Depurar JavaScript no Microsoft Edge Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixar Visual Studio 2019 para Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objeto de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Código"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para o Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos do Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentação webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Code Extension | documentação webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem do blog do Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"

> [!NOTE]
> <span data-ttu-id="895af-308">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="895af-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="895af-309">A página original é [encontrada](https://developers.google.com/web/updates/2019/12/devtools/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="895af-309">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="895af-311">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="895af-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
