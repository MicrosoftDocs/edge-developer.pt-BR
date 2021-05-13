---
description: Exibição 3D, Visual Studio integração com Microsoft Edge e muito mais.
title: Novidades no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 03b17f524e9be55e1ed37147ce46b7a15fc3a17d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564956"
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
# <a name="whats-new-in-devtools-microsoft-edge-81"></a><span data-ttu-id="ed404-104">Novidades no DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="ed404-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ed404-105">Comunicados da equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ed404-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="ed404-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed404-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="ed404-107">Confira os comunicados para experimentar novos recursos no DevTools, Microsoft Visual Studio Extensões de Código e muito mais.</span><span class="sxs-lookup"><span data-stu-id="ed404-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="ed404-108">Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais Microsoft Edge [de][MicrosoftEdgePreviewChannels] visualização e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="ed404-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="ed404-109">Melhorias de acessibilidade no DevTools</span><span class="sxs-lookup"><span data-stu-id="ed404-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="ed404-110">A equipe do DevTools contribuiu com 170 alterações no Chromium para resolver problemas de contraste de cores de alto impacto, teclado e leitor de tela no DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed404-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="ed404-111">Cada desenvolvedor que está criando a Web deve ser capaz de usar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed404-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="A ferramenta Performance no DevTools com as melhorias de navegação de teclado e leitor de tela" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="ed404-113">A **ferramenta Performance** no DevTools com as melhorias de navegação de teclado e leitor de tela</span><span class="sxs-lookup"><span data-stu-id="ed404-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-114">Quer saber como tornar sua página da Web acessível para todos os usuários?</span><span class="sxs-lookup"><span data-stu-id="ed404-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="ed404-115">Baixe os [Insights de Acessibilidade][AccessibilityInsights] e [extensões webhint][WebhintBrowserExtension] para Microsoft Edge para começar.</span><span class="sxs-lookup"><span data-stu-id="ed404-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="ed404-116">Se você usar leitores de tela ou o teclado para navegar [][PostTweetEdgeDevTools] ao redor do DevTools, envie seus comentários tuitando para nós ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="ed404-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="ed404-117">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="ed404-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="ed404-118">Usando o DevTools em outros idiomas</span><span class="sxs-lookup"><span data-stu-id="ed404-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="ed404-119">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code, em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="ed404-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="ed404-120">Estamos animados para anunciar a localização para o DevTools, que agora você pode usar em um dos 10 idiomas além do inglês:</span><span class="sxs-lookup"><span data-stu-id="ed404-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed404-121">Chinês \(Simplificado\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="ed404-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ed404-122">Chinês \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="ed404-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ed404-123">Francês –&#231;ais</span><span class="sxs-lookup"><span data-stu-id="ed404-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ed404-124">Alemão - deutsch</span><span class="sxs-lookup"><span data-stu-id="ed404-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ed404-125">Italiano - italiano</span><span class="sxs-lookup"><span data-stu-id="ed404-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ed404-126">Japonês - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="ed404-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ed404-127">Coreano - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="ed404-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ed404-128">Português - portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="ed404-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ed404-129">Russo – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="ed404-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ed404-130">Espanhol - espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="ed404-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="ed404-131">O DevTools corresponderá automaticamente ao idioma usado para Microsoft Edge em `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="ed404-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="ed404-132">Se você quiser Microsoft Edge em um idioma e seu DevTools permanecer em inglês, selecione no DevTools para abrir Configurações e desabilitar o idioma do navegador `F1` **match.** [][DevtoolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="ed404-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, select `F1` in the DevTools to open [Settings][DevtoolsCustomizeIndexSettings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="ed404-134">O DevTools em alemão</span><span class="sxs-lookup"><span data-stu-id="ed404-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-135">**As mensagens** de console não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="ed404-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="ed404-136">Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma usado para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ed404-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="ed404-137">Se você quiser usar o DevTools em um idioma diferente dos que estão disponíveis, [tweet][PostTweetEdgeDevTools] para nós ou escolha o [ícone Enviar Comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="ed404-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="ed404-138">Chromium problema [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="ed404-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="ed404-139">webhint Microsoft Edge extensão</span><span class="sxs-lookup"><span data-stu-id="ed404-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="ed404-140">A extensão webhint Microsoft Edge permite que você digitalizar facilmente sua página da Web e obter comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed404-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="ed404-141">Leia mais em [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="ed404-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="A ferramenta Hints no DevTools quando a extensão do navegador webhint é instalada" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="ed404-143">A **ferramenta Hints** no DevTools quando a extensão do navegador webhint é instalada</span><span class="sxs-lookup"><span data-stu-id="ed404-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-144">[Experimente a extensão do navegador webhint em Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="ed404-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="ed404-145">Depois de instalar a extensão, abra o DevTools e escolha a **ferramenta Dicas.**</span><span class="sxs-lookup"><span data-stu-id="ed404-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="ed404-146">A partir daqui, execute uma verificação de site personalizável.</span><span class="sxs-lookup"><span data-stu-id="ed404-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="ed404-147">Vá até [webhint.io][WebhintBrowserExtension] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="ed404-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <a name="3d-view"></a><span data-ttu-id="ed404-148">Modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="ed404-148">3D View</span></span>  

<span data-ttu-id="ed404-149">Use o **View 3D** para depurar seu aplicativo Web navegando pelo modelo de objeto de documento [\(DOM\)][MDNDocumentObjectModel] ou o contexto de empilhamento [de índice z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="ed404-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="A exibição 3D no DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="ed404-151">A exibição 3D no DevTools</span><span class="sxs-lookup"><span data-stu-id="ed404-151">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-152">Para acessar o View 3D, selecione `Ctrl`  +  `Shift`  +  `P` , digite No **3D View** e selecione **Mostrar Exibição 3D**.</span><span class="sxs-lookup"><span data-stu-id="ed404-152">To access the 3D View, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="ed404-153">A Microsoft Edge equipe está trabalhando com a equipe Chromium na interface do usuário e adicionando mais funcionalidade ao Modo de Exibição 3D, portanto, envie seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="ed404-153">The Microsoft Edge team is working with the Chromium team on the UI and adding more functionality to the 3D View, so please send your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="ed404-154">Chromium problema [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="ed404-154">Chromium issue [#987787][CR987787]</span></span>  

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="ed404-155">Visual Studio Code extensões</span><span class="sxs-lookup"><span data-stu-id="ed404-155">Visual Studio Code extensions</span></span>  

<span data-ttu-id="ed404-156">A equipe do DevTools também [][VisualStudioCode] lançou algumas extensões para Visual Studio Code que permitem que você use o poder do DevTools diretamente do editor de texto!</span><span class="sxs-lookup"><span data-stu-id="ed404-156">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="ed404-157">Confira as extensões abaixo:</span><span class="sxs-lookup"><span data-stu-id="ed404-157">Check out the extensions below:</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="ed404-158">Elementos para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ed404-158">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="ed404-159">Use a ferramenta Elements de dentro Visual Studio Code adicionando a extensão [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="ed404-159">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="A ferramenta Elements no Visual Studio Code usando os elementos para Microsoft Edge extensão" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="ed404-161">A **ferramenta Elements** no Visual Studio Code usando os elementos para Microsoft Edge extensão</span><span class="sxs-lookup"><span data-stu-id="ed404-161">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-162">Para obter mais informações, confira [Elementos para Microsoft Edge Visual Studio Code extensão][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="ed404-162">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="ed404-163">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ed404-163">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="ed404-164">Com o [Depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depure JavaScript em execução Microsoft Edge diretamente do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="ed404-164">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="O Depurador para Microsoft Edge Extension no Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="ed404-166">O Depurador para Microsoft Edge Extension no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ed404-166">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-167">Para obter mais informações, confira [como depurar][VisualStudioCodeDebuggerEdgeExtension]Microsoft Edge de Visual Studio Code .</span><span class="sxs-lookup"><span data-stu-id="ed404-167">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="ed404-168">Dica da web</span><span class="sxs-lookup"><span data-stu-id="ed404-168">webhint</span></span>  

<span data-ttu-id="ed404-169">A [extensão webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code usa `webhint` para melhorar sua página da Web enquanto você a escreve.</span><span class="sxs-lookup"><span data-stu-id="ed404-169">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you are writing it.</span></span>  <span data-ttu-id="ed404-170">Essa extensão é executado e relata diagnósticos em seus arquivos de espaço de trabalho com base na `webhint` análise.</span><span class="sxs-lookup"><span data-stu-id="ed404-170">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="O webhint Visual Studio Code extensão analisando um arquivo .tsx no Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="ed404-172">O webhint Visual Studio Code extensão analisando um `.tsx` arquivo no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ed404-172">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-173">[Saiba mais sobre a extensão Visual Studio Code webhint][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="ed404-173">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="ed404-174">Visual Studio integração</span><span class="sxs-lookup"><span data-stu-id="ed404-174">Visual Studio integration</span></span>  

<span data-ttu-id="ed404-175">No Visual Studio 2019 versão 16.2 ou posterior, use o depurador Visual Studio para depurar JavaScript em execução no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ed404-175">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="ed404-176">[Baixe Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso!</span><span class="sxs-lookup"><span data-stu-id="ed404-176">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio com a opção de iniciar seu aplicativo Web em Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="ed404-178">Visual Studio com a opção de iniciar seu aplicativo Web em Microsoft Edge Canary, Dev ou Beta</span><span class="sxs-lookup"><span data-stu-id="ed404-178">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-179">[Saiba mais sobre a depuração Microsoft Edge de Visual Studio][VisualStudioIndex].</span><span class="sxs-lookup"><span data-stu-id="ed404-179">[Learn more about debugging Microsoft Edge from Visual Studio][VisualStudioIndex].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="ed404-180">Acompanhamento de mensagens de console de prevenção</span><span class="sxs-lookup"><span data-stu-id="ed404-180">Tracking prevention Console messages</span></span>  

<span data-ttu-id="ed404-181">A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você de ser rastreado por sites que você não visitou antes.</span><span class="sxs-lookup"><span data-stu-id="ed404-181">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you have not visited before.</span></span>  <span data-ttu-id="ed404-182">A configuração de prevenção de rastreamento padrão é o modo Balanceado, que bloqueia rastreadores de terceiros e rastreadores mal-intencionados conhecidos para uma experiência que equilibra a privacidade e a compatibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="ed404-182">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="ed404-183">Para dar mais informações sobre a compatibilidade da página da Web quando determinados rastreadores são bloqueados, as mensagens de aviso foram adicionadas ao **Console** quando um rastreador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ed404-183">To give you more insight into the compatibility of your web page when certain trackers are blocked, warning messages were added in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensagens no Console quando o controle de prevenção bloqueia o acesso ao armazenamento de um rastreador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="ed404-185">Mensagens no **Console quando o controle** de prevenção bloqueia o acesso ao armazenamento de um rastreador</span><span class="sxs-lookup"><span data-stu-id="ed404-185">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-186">[Leia mais sobre como controlar a prevenção e o equilíbrio entre privacidade e compatibilidade com a Web.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="ed404-186">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="ed404-187">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="ed404-187">Announcements from the Chromium project</span></span>  

<span data-ttu-id="ed404-188">As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 81 que foram contribuídos para o projeto de Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="ed404-188">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <a name="moto-g4-support-in-device-mode"></a><span data-ttu-id="ed404-189">Suporte ao Moto G4 no Modo de Dispositivo</span><span class="sxs-lookup"><span data-stu-id="ed404-189">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="ed404-190">Depois [de habiltar][DevtoolsDeviceModeIndexSimulateMobileViewport]a Barra de Ferramentas de Dispositivo, simule as dimensões de um viewport do Moto G4 na **lista Dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ed404-190">After [enabling the Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulando um viewport do Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="ed404-192">Simulando um viewport do Moto G4</span><span class="sxs-lookup"><span data-stu-id="ed404-192">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-193">Escolha [Mostrar Quadro de Dispositivo][DevtoolsDeviceModeIndexShowDeviceFrame] para mostrar o hardware do Moto G4 ao redor do viewport.</span><span class="sxs-lookup"><span data-stu-id="ed404-193">Choose [Show Device Frame][DevtoolsDeviceModeIndexShowDeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrando o hardware do Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="ed404-195">Mostrando o hardware do Moto G4</span><span class="sxs-lookup"><span data-stu-id="ed404-195">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-196">Recursos relacionados:</span><span class="sxs-lookup"><span data-stu-id="ed404-196">Related features:</span></span>  

*   <span data-ttu-id="ed404-197">Abra o [Menu de Comando][DevtoolsCommandMenuIndex] e execute o comando para fazer uma captura de tela do viewport que inclui o hardware do Moto G4 (depois de habiltar `Capture screenshot` **Show Device Frame**).</span><span class="sxs-lookup"><span data-stu-id="ed404-197">Open the [Command Menu][DevtoolsCommandMenuIndex] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="ed404-198">[Acelere a rede e a CPU][DevtoolsDeviceModeIndexThrottleNetworkCpu] para simular com mais precisão as condições de navegação da Web de um usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="ed404-198">[Throttle the network and CPU][DevtoolsDeviceModeIndexThrottleNetworkCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="ed404-199">Chromium problema [#924693][CR924693]</span><span class="sxs-lookup"><span data-stu-id="ed404-199">Chromium issue [#924693][CR924693]</span></span>  

### <a name="cookie-related-updates"></a><span data-ttu-id="ed404-200">Atualizações relacionadas a cookies</span><span class="sxs-lookup"><span data-stu-id="ed404-200">Cookie-related updates</span></span>  

#### <a name="blocked-cookies-in-the-cookies-pane"></a><span data-ttu-id="ed404-201">Cookies bloqueados no painel Cookies</span><span class="sxs-lookup"><span data-stu-id="ed404-201">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="ed404-202">O painel Cookies no painel Aplicativo agora exibe cookies bloqueados com um plano de fundo amarelo.</span><span class="sxs-lookup"><span data-stu-id="ed404-202">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueados no painel Cookies do painel Aplicativo" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="ed404-204">Cookies bloqueados no painel Cookies do painel Aplicativo</span><span class="sxs-lookup"><span data-stu-id="ed404-204">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-205">Chromium problema [#1030258][CR1030258]</span><span class="sxs-lookup"><span data-stu-id="ed404-205">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a><span data-ttu-id="ed404-206">Prioridade de cookie no painel Cookie</span><span class="sxs-lookup"><span data-stu-id="ed404-206">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="ed404-207">As tabelas Cookies nas **ferramentas Rede** **e Aplicativo** agora incluem uma **coluna Priority.**</span><span class="sxs-lookup"><span data-stu-id="ed404-207">The Cookies tables in the **Network** and **Application** tools now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="ed404-208">Chromium navegadores baseados em cookies, como Microsoft Edge, são os únicos navegadores que suportam prioridade de cookie.</span><span class="sxs-lookup"><span data-stu-id="ed404-208">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="ed404-209">Chromium problema [#1026879][CR1026879]</span><span class="sxs-lookup"><span data-stu-id="ed404-209">Chromium issue [#1026879][CR1026879]</span></span>  

#### <a name="edit-all-cookie-values"></a><span data-ttu-id="ed404-210">Editar todos os valores de cookie</span><span class="sxs-lookup"><span data-stu-id="ed404-210">Edit all cookie values</span></span>  

<span data-ttu-id="ed404-211">Todas as células nas tabelas Cookie agora podem ser editadas, exceto células na coluna **Tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ed404-211">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="ed404-212">Para uma explicação de cada coluna, navegue até [Campos][DevtoolsStorageCookiesFields].</span><span class="sxs-lookup"><span data-stu-id="ed404-212">For an explanation of each column, navigate to [Fields][DevtoolsStorageCookiesFields].</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Editar um valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="ed404-214">Editar um valor de cookie</span><span class="sxs-lookup"><span data-stu-id="ed404-214">Editing a cookie value</span></span>  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a><span data-ttu-id="ed404-215">Copiar como Node.js buscar para incluir dados de cookie</span><span class="sxs-lookup"><span data-stu-id="ed404-215">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="ed404-216">Para obter uma expressão que inclua dados de cookie, passe o mouse em uma solicitação de rede, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar Cópia como Node.js `fetch` \*\*\*\*  >  **buscar**.</span><span class="sxs-lookup"><span data-stu-id="ed404-216">To get a `fetch` expression that includes cookie data, hover on a network request, open the contextual menu \(right-click\), and choose **Copy** > **Copy as Node.js fetch**.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js busca" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="ed404-218">Copiar como Node.js busca</span><span class="sxs-lookup"><span data-stu-id="ed404-218">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-219">Chromium problema [#1029826][CR1029826]</span><span class="sxs-lookup"><span data-stu-id="ed404-219">Chromium issue [#1029826][CR1029826]</span></span>  

### <a name="more-accurate-web-app-manifest-icons"></a><span data-ttu-id="ed404-220">Ícones de manifesto de aplicativo web mais precisos</span><span class="sxs-lookup"><span data-stu-id="ed404-220">More accurate web app manifest icons</span></span>  

<span data-ttu-id="ed404-221">Anteriormente, o painel Manifesto no painel Aplicativo enviava suas próprias solicitações para exibir ícones de manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="ed404-221">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="ed404-222">O DevTools agora mostra o mesmo ícone de manifesto que Microsoft Edge usa.</span><span class="sxs-lookup"><span data-stu-id="ed404-222">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Ícones no painel Manifesto" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="ed404-224">Ícones no painel Manifesto</span><span class="sxs-lookup"><span data-stu-id="ed404-224">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-225">Chromium problema [#985402][CR985402]</span><span class="sxs-lookup"><span data-stu-id="ed404-225">Chromium issue [#985402][CR985402]</span></span>  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a><span data-ttu-id="ed404-226">Passe o mouse em propriedades de conteúdo CSS para exibir valores não-escapados</span><span class="sxs-lookup"><span data-stu-id="ed404-226">Hover on CSS content properties to display unescaped values</span></span>  

<span data-ttu-id="ed404-227">Passe o mouse no valor de uma propriedade para exibir a versão não `content` paisagem do valor.</span><span class="sxs-lookup"><span data-stu-id="ed404-227">Hover on the value of a `content` property to display the unescaped version of the value.</span></span>  

<span data-ttu-id="ed404-228">Por exemplo, nesta [demonstração][CSSContentDemo] quando você inspeciona o pseudo-elemento, uma cadeia de caracteres de escape `p::after` é exibida no painel **Estilos:**</span><span class="sxs-lookup"><span data-stu-id="ed404-228">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element an escaped string is displayed in the **Styles** pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="A cadeia de caracteres de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="ed404-230">A cadeia de caracteres de escape</span><span class="sxs-lookup"><span data-stu-id="ed404-230">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="ed404-231">Quando você passar o mouse sobre `content` o valor, o valor não escapou é exibido.</span><span class="sxs-lookup"><span data-stu-id="ed404-231">When you hover on the `content` value, the unescaped value is displayed.</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="O valor não-escapado" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="ed404-233">O valor não-escapado</span><span class="sxs-lookup"><span data-stu-id="ed404-233">The unescaped value</span></span>  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a><span data-ttu-id="ed404-234">Erros de mapa de origem mais detalhados no Console</span><span class="sxs-lookup"><span data-stu-id="ed404-234">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="ed404-235">O Console agora fornece mais detalhes sobre por que um mapa de origem falhou ao carregar ou analisar.</span><span class="sxs-lookup"><span data-stu-id="ed404-235">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="ed404-236">Anteriormente, ele apenas forneceu um erro sem explicar o que deu errado.</span><span class="sxs-lookup"><span data-stu-id="ed404-236">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Um erro de carregamento de mapa de origem no Console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="ed404-238">Um erro de carregamento de mapa de origem no Console</span><span class="sxs-lookup"><span data-stu-id="ed404-238">A source map loading error in the Console</span></span>  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a><span data-ttu-id="ed404-239">Configuração para desabilitar a rolagem após o final de um arquivo</span><span class="sxs-lookup"><span data-stu-id="ed404-239">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="ed404-240">Abra [Configurações][DevtoolsCustomizeIndexSettings] e desabilite Fontes de **Preferências**Permitir rolagem no final do arquivo para desabilitar o comportamento padrão da interface do usuário que permite que você role bem além do final de um arquivo no painel  >  \*\*\*\*  >  \*\*\*\* **Fontes.**</span><span class="sxs-lookup"><span data-stu-id="ed404-240">Open [Settings][DevtoolsCustomizeIndexSettings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Desabilitar Permitir a rolagem do final passado do arquivo" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="ed404-242">Desabilitar **Permitir a rolagem do final do arquivo no** Configurações</span><span class="sxs-lookup"><span data-stu-id="ed404-242">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="A rolagem além do final de um arquivo agora está desabilitada no painel Fontes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="ed404-244">A rolagem além do final de um arquivo agora está desabilitada no painel Fontes</span><span class="sxs-lookup"><span data-stu-id="ed404-244">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="ed404-245">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ed404-245">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="ed404-246">Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="ed404-246">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="ed404-247">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed404-247">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="ed404-248">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ed404-248">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular um modo de exibição móvel - Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsDeviceModeIndexShowDeviceFrame]: ../../../device-mode/index.md#show-device-frame "Mostrar quadro do dispositivo - Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexThrottleNetworkCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Acelerar a rede e a CPU - Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsStorageCookiesFields]: ../../../storage/cookies.md#fields "Campos - Exibir, editar e excluir cookies com Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioIndex]: ../../../../visual-studio/index.md "Visual Studio | Microsoft Docs"  

[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos para Microsoft Edge \(Chromium\) | Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"

[TrackingPrevention]: https://blogs.windows.com/msedgedev/2019/12/03/improving-tracking-prevention-microsoft-edge-79 "Melhorando a prevenção de rastreamento Microsoft Edge postagem no blog"

[MicrosoftEdgeInsiderAddons]: https://microsoftedge.microsoft.com/addons/detail/webhint/mlgfbihcfnkaenjpdcngdnhcpkdmcdee "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Baixar Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um Tweet"  

[CR924693]: https://crbug.com/924693 "Solicitação de Recurso: Adicionar o Moto G4 à lista de | Chromium Bugs"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Chromium Bugs"  
[CR1026879]: https://crbug.com/1026879 "A guia Cookie no console de dev não mostra mais a prioridade | Chromium Bugs"  
[CR1029826]: https://crbug.com/1029826 "guia de rede -> escolha solicitar -> cópia -> cópia como busca não copia cookies | Chromium Bugs"  
[CR985402]: https://crbug.com/985402 "Cadeias de erro de ícone de manifesto do aplicativo web são confusas | Chromium Bugs"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Chromium Bugs"  
[CR941561]: https://crbug.com/941561 "Localizabilidade do devTools | Chromium Bugs"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração para conteúdo CSS sem paisagem"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

[TheWebWeWant]: https://webwewant.fyi "A Web que queremos"  
[AccessibilityInsights]: https://accessibilityinsights.io "Percepções de acessibilidade"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objeto de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "conta @EdgeDevTools do Twitter"  

[Webhint]: https://webhint.io "webhint"  

[WebhintBrowserExtension]: https://webhint.io/docs/user-guide/extensions/extension-browser "Webhint Browser Extension | documentação webhint"  
[WebhintVisualStudioCodeExtension]: https://webhint.io/docs/user-guide/extensions/vscode-webhint "Webhint Visual Studio Code Extension | documentação webhint"  

> [!NOTE]
> <span data-ttu-id="ed404-285">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ed404-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ed404-286">A página original é [encontrada](https://developer.chrome.com/blog/new-in-devtools-81) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="ed404-286">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-81) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ed404-288">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ed404-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  