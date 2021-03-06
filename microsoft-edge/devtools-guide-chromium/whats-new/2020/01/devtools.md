---
description: Exibição 3D, Visual Studio integração com o Microsoft Edge e muito mais.
title: Novidades no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a60be4d55d7f6152ed7ce7afd24049f0f5909a4b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398242"
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

# <a name="whats-new-in-devtools-microsoft-edge-81"></a><span data-ttu-id="2f6ca-104">Novidades no DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="2f6ca-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2f6ca-105">Comunicados da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2f6ca-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="2f6ca-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="2f6ca-107">Confira os comunicados para experimentar novos recursos no DevTools, no Microsoft Visual Studio Code e muito mais.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="2f6ca-108">Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="2f6ca-109">Melhorias de acessibilidade no DevTools</span><span class="sxs-lookup"><span data-stu-id="2f6ca-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="2f6ca-110">A equipe do DevTools contribuiu com 170 alterações no Chromium para resolver problemas de contraste de cores de alto impacto, teclado e leitor de tela no DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="2f6ca-111">Cada desenvolvedor que está criando a Web deve ser capaz de usar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="A ferramenta Performance no DevTools com as melhorias de navegação de teclado e leitor de tela" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="2f6ca-113">A **ferramenta Performance** no DevTools com as melhorias de navegação de teclado e leitor de tela</span><span class="sxs-lookup"><span data-stu-id="2f6ca-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-114">Quer saber como tornar sua página da Web acessível para todos os usuários?</span><span class="sxs-lookup"><span data-stu-id="2f6ca-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="2f6ca-115">Baixe as [Percepções de Acessibilidade][AccessibilityInsights] [e extensões webhint][WebhintBrowserExtension] do Microsoft Edge para começar.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="2f6ca-116">Se você usar leitores de tela ou o teclado para navegar [][PostTweetEdgeDevTools] ao redor do DevTools, envie seus comentários tuitando para nós ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="2f6ca-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="2f6ca-117">Problema do Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="2f6ca-118">Usando o DevTools em outros idiomas</span><span class="sxs-lookup"><span data-stu-id="2f6ca-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="2f6ca-119">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code, em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="2f6ca-120">Estamos animados para anunciar a localização para o DevTools, que agora você pode usar em um dos 10 idiomas além do inglês:</span><span class="sxs-lookup"><span data-stu-id="2f6ca-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2f6ca-121">Chinês \(Simplificado\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2f6ca-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f6ca-122">Chinês \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2f6ca-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f6ca-123">Francês –&#231;ais</span><span class="sxs-lookup"><span data-stu-id="2f6ca-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f6ca-124">Alemão - deutsch</span><span class="sxs-lookup"><span data-stu-id="2f6ca-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f6ca-125">Italiano - italiano</span><span class="sxs-lookup"><span data-stu-id="2f6ca-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f6ca-126">Japonês - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="2f6ca-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f6ca-127">Coreano - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="2f6ca-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f6ca-128">Português - portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="2f6ca-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f6ca-129">Russo – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="2f6ca-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f6ca-130">Espanhol - espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="2f6ca-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="2f6ca-131">O DevTools corresponderá automaticamente ao idioma que você usa para o Microsoft Edge em `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="2f6ca-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="2f6ca-132">Se você quiser que o Microsoft Edge fique em um idioma e seu DevTools permaneça em inglês, selecione no DevTools para abrir Configurações e desabilitar Corresponder idioma `F1` **do navegador**. [][Settings]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, select `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="2f6ca-134">O DevTools em alemão</span><span class="sxs-lookup"><span data-stu-id="2f6ca-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-135">**As mensagens** de console não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="2f6ca-136">Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma que você usa para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="2f6ca-137">Se você quiser usar o DevTools em um idioma diferente dos que estão disponíveis, [tweet][PostTweetEdgeDevTools] para nós ou escolha o [ícone Enviar Comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="2f6ca-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="2f6ca-138">Problema do Chromium [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="2f6ca-139">extensão webhint do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f6ca-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="2f6ca-140">A extensão webhint do Microsoft Edge permite que você digitalizar facilmente sua página da Web e obter comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="2f6ca-141">Leia mais em [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="2f6ca-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="A ferramenta Hints no DevTools quando a extensão do navegador webhint é instalada" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="2f6ca-143">A **ferramenta Hints** no DevTools quando a extensão do navegador webhint é instalada</span><span class="sxs-lookup"><span data-stu-id="2f6ca-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-144">[Experimente a extensão do navegador webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="2f6ca-145">Depois de instalar a extensão, abra o DevTools e escolha a **ferramenta Dicas.**</span><span class="sxs-lookup"><span data-stu-id="2f6ca-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="2f6ca-146">A partir daqui, execute uma verificação de site personalizável.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="2f6ca-147">Vá até [webhint.io][WebhintBrowserExtension] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <a name="3d-view"></a><span data-ttu-id="2f6ca-148">Modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="2f6ca-148">3D View</span></span>  

<span data-ttu-id="2f6ca-149">Use o **View 3D** para depurar seu aplicativo Web navegando pelo modelo de objeto de documento [\(DOM\)][MDNDocumentObjectModel] ou o contexto de empilhamento [de índice z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="A exibição 3D no DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="2f6ca-151">A exibição 3D no DevTools</span><span class="sxs-lookup"><span data-stu-id="2f6ca-151">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-152">Para acessar o View 3D, selecione `Ctrl`  +  `Shift`  +  `P` , digite No **3D View** e selecione **Mostrar Exibição 3D**.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-152">To access the 3D View, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="2f6ca-153">A equipe do Microsoft Edge está trabalhando com a equipe do Chromium na interface do usuário e adicionando mais funcionalidade ao Modo de Exibição 3D, portanto, envie seus [comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="2f6ca-153">The Microsoft Edge team is working with the Chromium team on the UI and adding more functionality to the 3D View, so please send your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="2f6ca-154">Problema do Chromium [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-154">Chromium issue [#987787][CR987787]</span></span>  

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="2f6ca-155">Visual Studio extensões de código</span><span class="sxs-lookup"><span data-stu-id="2f6ca-155">Visual Studio Code extensions</span></span>  

<span data-ttu-id="2f6ca-156">A equipe do DevTools também lançou algumas extensões para Visual Studio [Code][VisualStudioCode] que permitem que você use o poder do DevTools diretamente do seu editor de texto!</span><span class="sxs-lookup"><span data-stu-id="2f6ca-156">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="2f6ca-157">Confira as extensões abaixo:</span><span class="sxs-lookup"><span data-stu-id="2f6ca-157">Check out the extensions below:</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="2f6ca-158">Elementos para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f6ca-158">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="2f6ca-159">Use a ferramenta Elements de dentro Visual Studio Code adicionando a extensão [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-159">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="A ferramenta Elements no Visual Studio Code usando a extensão Elements for Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="2f6ca-161">A **ferramenta Elements** no Visual Studio Code usando a extensão Elements for Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f6ca-161">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-162">Para obter mais informações, confira [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-162">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="2f6ca-163">Depurador para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f6ca-163">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="2f6ca-164">Com a [extensão Depurador do Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depure JavaScript em execução no Microsoft Edge diretamente do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-164">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="O Depurador para a Extensão do Microsoft Edge em Visual Studio Código" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="2f6ca-166">O Depurador para a Extensão do Microsoft Edge em Visual Studio Código</span><span class="sxs-lookup"><span data-stu-id="2f6ca-166">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-167">Para obter mais informações, confira [como depurar o Microsoft Edge de Visual Studio Código][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-167">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="2f6ca-168">Dica da web</span><span class="sxs-lookup"><span data-stu-id="2f6ca-168">webhint</span></span>  

<span data-ttu-id="2f6ca-169">A [extensão webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code usa `webhint` para melhorar sua página da Web enquanto você a escreve.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-169">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you are writing it.</span></span>  <span data-ttu-id="2f6ca-170">Essa extensão é executado e relata diagnósticos em seus arquivos de espaço de trabalho com base na `webhint` análise.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-170">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="A extensão webhint Visual Studio Code analisando um arquivo .tsx em Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="2f6ca-172">A extensão webhint Visual Studio Code analisando um `.tsx` arquivo em Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2f6ca-172">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-173">[Saiba mais sobre a extensão webhint Visual Studio Code][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-173">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="2f6ca-174">Visual Studio integração</span><span class="sxs-lookup"><span data-stu-id="2f6ca-174">Visual Studio integration</span></span>  

<span data-ttu-id="2f6ca-175">No Visual Studio 2019 versão 16.2 ou posterior, use o depurador Visual Studio para depurar JavaScript em execução no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-175">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="2f6ca-176">[Baixe Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso!</span><span class="sxs-lookup"><span data-stu-id="2f6ca-176">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="2f6ca-178">Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canary, Dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="2f6ca-178">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-179">[Saiba mais sobre a depuração do Microsoft Edge Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-179">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="2f6ca-180">Acompanhamento de mensagens de console de prevenção</span><span class="sxs-lookup"><span data-stu-id="2f6ca-180">Tracking prevention Console messages</span></span>  

<span data-ttu-id="2f6ca-181">A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você de ser rastreado por sites que você não visitou antes.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-181">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you have not visited before.</span></span>  <span data-ttu-id="2f6ca-182">A configuração de prevenção de rastreamento padrão é o modo Balanceado, que bloqueia rastreadores de terceiros e rastreadores mal-intencionados conhecidos para uma experiência que equilibra a privacidade e a compatibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-182">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="2f6ca-183">Para dar mais informações sobre a compatibilidade da página da Web quando determinados rastreadores são bloqueados, as mensagens de aviso foram adicionadas ao **Console** quando um rastreador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-183">To give you more insight into the compatibility of your web page when certain trackers are blocked, warning messages were added in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensagens no Console quando o controle de prevenção bloqueia o acesso ao armazenamento de um rastreador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="2f6ca-185">Mensagens no **Console quando o controle** de prevenção bloqueia o acesso ao armazenamento de um rastreador</span><span class="sxs-lookup"><span data-stu-id="2f6ca-185">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-186">[Leia mais sobre como controlar a prevenção e o equilíbrio entre privacidade e compatibilidade com a Web.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-186">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="2f6ca-187">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="2f6ca-187">Announcements from the Chromium project</span></span>  

<span data-ttu-id="2f6ca-188">As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 81 que contribuíram para o projeto Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-188">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <a name="moto-g4-support-in-device-mode"></a><span data-ttu-id="2f6ca-189">Suporte ao Moto G4 no Modo de Dispositivo</span><span class="sxs-lookup"><span data-stu-id="2f6ca-189">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="2f6ca-190">Depois [de habiltar][DeviceToolbar]a Barra de Ferramentas de Dispositivo, simule as dimensões de um viewport do Moto G4 na **lista Dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2f6ca-190">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulando um viewport do Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="2f6ca-192">Simulando um viewport do Moto G4</span><span class="sxs-lookup"><span data-stu-id="2f6ca-192">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-193">Escolha [Mostrar Quadro de Dispositivo][DeviceFrame] para mostrar o hardware do Moto G4 ao redor do viewport.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-193">Choose [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrando o hardware do Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="2f6ca-195">Mostrando o hardware do Moto G4</span><span class="sxs-lookup"><span data-stu-id="2f6ca-195">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-196">Recursos relacionados:</span><span class="sxs-lookup"><span data-stu-id="2f6ca-196">Related features:</span></span>  

*   <span data-ttu-id="2f6ca-197">Abra o [Menu de Comando][CommandMenu] e execute o comando para fazer uma captura de tela do viewport que inclui o hardware do Moto G4 (depois de habiltar `Capture screenshot` **Show Device Frame**).</span><span class="sxs-lookup"><span data-stu-id="2f6ca-197">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="2f6ca-198">[Acelere a rede e a CPU][ThrottleNetworkAndCpu] para simular com mais precisão as condições de navegação da Web de um usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-198">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="2f6ca-199">Problema do Chromium [#924693][CR924693]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-199">Chromium issue [#924693][CR924693]</span></span>  

### <a name="cookie-related-updates"></a><span data-ttu-id="2f6ca-200">Atualizações relacionadas a cookies</span><span class="sxs-lookup"><span data-stu-id="2f6ca-200">Cookie-related updates</span></span>  

#### <a name="blocked-cookies-in-the-cookies-pane"></a><span data-ttu-id="2f6ca-201">Cookies bloqueados no painel Cookies</span><span class="sxs-lookup"><span data-stu-id="2f6ca-201">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="2f6ca-202">O painel Cookies no painel Aplicativo agora exibe cookies bloqueados com um plano de fundo amarelo.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-202">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueados no painel Cookies do painel Aplicativo" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="2f6ca-204">Cookies bloqueados no painel Cookies do painel Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2f6ca-204">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-205">Problema do Chromium [#1030258][CR1030258]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-205">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a><span data-ttu-id="2f6ca-206">Prioridade de cookie no painel Cookie</span><span class="sxs-lookup"><span data-stu-id="2f6ca-206">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="2f6ca-207">As tabelas Cookies nas **ferramentas Rede** **e Aplicativo** agora incluem uma **coluna Priority.**</span><span class="sxs-lookup"><span data-stu-id="2f6ca-207">The Cookies tables in the **Network** and **Application** tools now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2f6ca-208">Os navegadores baseados em Chromium, como o Microsoft Edge, são os únicos navegadores que suportam prioridade de cookie.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-208">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="2f6ca-209">Problema do Chromium [#1026879][CR1026879]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-209">Chromium issue [#1026879][CR1026879]</span></span>  

#### <a name="edit-all-cookie-values"></a><span data-ttu-id="2f6ca-210">Editar todos os valores de cookie</span><span class="sxs-lookup"><span data-stu-id="2f6ca-210">Edit all cookie values</span></span>  

<span data-ttu-id="2f6ca-211">Todas as células nas tabelas Cookie agora podem ser editadas, exceto células na coluna **Tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-211">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="2f6ca-212">Para uma explicação de cada coluna, navegue até [Campos][CookiesFields].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-212">For an explanation of each column, navigate to [Fields][CookiesFields].</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Editar um valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="2f6ca-214">Editar um valor de cookie</span><span class="sxs-lookup"><span data-stu-id="2f6ca-214">Editing a cookie value</span></span>  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a><span data-ttu-id="2f6ca-215">Copiar como Node.js buscar para incluir dados de cookie</span><span class="sxs-lookup"><span data-stu-id="2f6ca-215">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="2f6ca-216">Para obter uma expressão que inclua dados de cookie, passe o mouse em uma solicitação de rede, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar Cópia como Node.js `fetch` \*\*\*\*  >  **buscar**.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-216">To get a `fetch` expression that includes cookie data, hover on a network request, open the contextual menu \(right-click\), and choose **Copy** > **Copy as Node.js fetch**.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js busca" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="2f6ca-218">Copiar como Node.js busca</span><span class="sxs-lookup"><span data-stu-id="2f6ca-218">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-219">Problema do Chromium [#1029826][CR1029826]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-219">Chromium issue [#1029826][CR1029826]</span></span>  

### <a name="more-accurate-web-app-manifest-icons"></a><span data-ttu-id="2f6ca-220">Ícones de manifesto de aplicativo web mais precisos</span><span class="sxs-lookup"><span data-stu-id="2f6ca-220">More accurate web app manifest icons</span></span>  

<span data-ttu-id="2f6ca-221">Anteriormente, o painel Manifesto no painel Aplicativo enviava suas próprias solicitações para exibir ícones de manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-221">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="2f6ca-222">O DevTools agora mostra o mesmo ícone de manifesto que o Microsoft Edge usa.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-222">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Ícones no painel Manifesto" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="2f6ca-224">Ícones no painel Manifesto</span><span class="sxs-lookup"><span data-stu-id="2f6ca-224">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-225">Problema do Chromium [#985402][CR985402]</span><span class="sxs-lookup"><span data-stu-id="2f6ca-225">Chromium issue [#985402][CR985402]</span></span>  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a><span data-ttu-id="2f6ca-226">Passe o mouse em propriedades de conteúdo CSS para exibir valores não-escapados</span><span class="sxs-lookup"><span data-stu-id="2f6ca-226">Hover on CSS content properties to display unescaped values</span></span>  

<span data-ttu-id="2f6ca-227">Passe o mouse no valor de uma propriedade para exibir a versão não `content` paisagem do valor.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-227">Hover on the value of a `content` property to display the unescaped version of the value.</span></span>  

<span data-ttu-id="2f6ca-228">Por exemplo, nesta [demonstração][CSSContentDemo] quando você inspeciona o pseudo-elemento, uma cadeia de caracteres de escape `p::after` é exibida no painel **Estilos:**</span><span class="sxs-lookup"><span data-stu-id="2f6ca-228">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element an escaped string is displayed in the **Styles** pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="A cadeia de caracteres de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="2f6ca-230">A cadeia de caracteres de escape</span><span class="sxs-lookup"><span data-stu-id="2f6ca-230">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="2f6ca-231">Quando você passar o mouse sobre `content` o valor, o valor não escapou é exibido.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-231">When you hover on the `content` value, the unescaped value is displayed.</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="O valor não-escapado" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="2f6ca-233">O valor não-escapado</span><span class="sxs-lookup"><span data-stu-id="2f6ca-233">The unescaped value</span></span>  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a><span data-ttu-id="2f6ca-234">Erros de mapa de origem mais detalhados no Console</span><span class="sxs-lookup"><span data-stu-id="2f6ca-234">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="2f6ca-235">O Console agora fornece mais detalhes sobre por que um mapa de origem falhou ao carregar ou analisar.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-235">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="2f6ca-236">Anteriormente, ele apenas forneceu um erro sem explicar o que deu errado.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-236">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Um erro de carregamento de mapa de origem no Console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="2f6ca-238">Um erro de carregamento de mapa de origem no Console</span><span class="sxs-lookup"><span data-stu-id="2f6ca-238">A source map loading error in the Console</span></span>  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a><span data-ttu-id="2f6ca-239">Configuração para desabilitar a rolagem após o final de um arquivo</span><span class="sxs-lookup"><span data-stu-id="2f6ca-239">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="2f6ca-240">Abra [Configurações][Settings] e desabilite Fontes de **Preferências**Permitir rolagem no final do arquivo para desabilitar o comportamento padrão da interface do usuário que permite que você role bem além do final de um arquivo no painel  >  \*\*\*\*  >  \*\*\*\* **Fontes.**</span><span class="sxs-lookup"><span data-stu-id="2f6ca-240">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Desabilitar Permitir a rolagem do final passado do arquivo" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="2f6ca-242">Desabilitar **Permitir a rolagem do final passado do arquivo** em Configurações</span><span class="sxs-lookup"><span data-stu-id="2f6ca-242">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="A rolagem além do final de um arquivo agora está desabilitada no painel Fontes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="2f6ca-244">A rolagem além do final de um arquivo agora está desabilitada no painel Fontes</span><span class="sxs-lookup"><span data-stu-id="2f6ca-244">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="2f6ca-245">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f6ca-245">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="2f6ca-246">Se você estiver no Windows ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-246">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2f6ca-247">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f6ca-247">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="2f6ca-248">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2f6ca-248">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular um modo de exibição móvel - Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Docs"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Mostrar quadro do dispositivo - Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Docs"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Execute comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Acelerar a rede e a CPU - Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Docs"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Microsoft Docs"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Campos - Exibir, editar e excluir cookies com o Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para a extensão Visual Studio Código do Microsoft Edge"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos para a extensão Visual Studio Código do Microsoft Edge"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Código"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para o Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos do Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem do blog do Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixar Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um Tweet"  

[CR924693]: https://crbug.com/924693 "Solicitação de Recurso: Adicionar o Moto G4 à lista de | Bugs de cromo"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Bugs de cromo"  
[CR1026879]: https://crbug.com/1026879 "A guia Cookie no console de dev não mostra mais a prioridade | Bugs de cromo"  
[CR1029826]: https://crbug.com/1029826 "guia de rede -> escolha solicitar -> cópia -> cópia como busca não copia cookies | Bugs de cromo"  
[CR985402]: https://crbug.com/985402 "Cadeias de erro de ícone de manifesto do aplicativo web são confusas | Bugs de cromo"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Bugs de cromo"  
[CR941561]: https://crbug.com/941561 "Localizabilidade do devTools | Bugs de cromo"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Bugs de cromo"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração para conteúdo CSS sem paisagem"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Percepções de acessibilidade"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objeto de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentação webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Code Extension | documentação webhint"  

> [!NOTE]
> <span data-ttu-id="2f6ca-285">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2f6ca-286">A página original é [encontrada](https://developers.google.com/web/updates/2020/01/devtools/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2f6ca-286">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2f6ca-288">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f6ca-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  