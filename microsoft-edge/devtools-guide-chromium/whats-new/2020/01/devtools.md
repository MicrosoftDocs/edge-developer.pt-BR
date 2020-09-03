---
description: Modo de exibição 3D, integração do Visual Studio com o Microsoft Edge e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 9dd47a38f345601f2d459d39e3ee7b1728df8971
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993412"
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

# <span data-ttu-id="77f51-104">O que há de novo no DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="77f51-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="77f51-105">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="77f51-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="77f51-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="77f51-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="77f51-107">Dê uma olhada neles para experimentar os novos recursos do DevTools, as extensões de código do VS e muito mais.</span><span class="sxs-lookup"><span data-stu-id="77f51-107">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="77f51-108">Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="77f51-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="77f51-109">Melhorias de acessibilidade no DevTools</span><span class="sxs-lookup"><span data-stu-id="77f51-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="77f51-110">A equipe do DevTools contribuiu com as mudanças do 170 para o Chromium para solucionar problemas de cor de alto impacto, teclado e leitor de tela no DevTools.</span><span class="sxs-lookup"><span data-stu-id="77f51-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="77f51-111">Cada desenvolvedor que cria a Web deve poder usar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="77f51-111">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="77f51-112">Figura 1</span><span class="sxs-lookup"><span data-stu-id="77f51-112">Figure 1</span></span>  
> <span data-ttu-id="77f51-113">A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela</span><span class="sxs-lookup"><span data-stu-id="77f51-113">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="77f51-115">Deseja saber como tornar sua página da Web acessível a todos os seus usuários?</span><span class="sxs-lookup"><span data-stu-id="77f51-115">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="77f51-116">Baixe as [informações sobre acessibilidade][AccessibilityInsights] e as extensões [webhint][WebhintBrowserExtension] para o Microsoft Edge para começar.</span><span class="sxs-lookup"><span data-stu-id="77f51-116">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="77f51-117">Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="77f51-117">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="77f51-118">Chromium problema [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="77f51-118">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="77f51-119">Usando o DevTools em outros idiomas</span><span class="sxs-lookup"><span data-stu-id="77f51-119">Using the DevTools in other languages</span></span>  

<span data-ttu-id="77f51-120">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e código VS, em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="77f51-120">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="77f51-121">Estamos entusiasmados a anunciar a localização do DevTools, que agora você pode usar em um dos dez idiomas além do inglês:</span><span class="sxs-lookup"><span data-stu-id="77f51-121">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="77f51-122">Chinês \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="77f51-122">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77f51-123">Chinês \ (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="77f51-123">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77f51-124">Francês – Fran-Fran&#231;ais</span><span class="sxs-lookup"><span data-stu-id="77f51-124">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77f51-125">Alemão – Deutsch</span><span class="sxs-lookup"><span data-stu-id="77f51-125">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77f51-126">Italiano-Italiano</span><span class="sxs-lookup"><span data-stu-id="77f51-126">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77f51-127"> &#26085;&#26412;&#35486; japonês</span><span class="sxs-lookup"><span data-stu-id="77f51-127">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77f51-128">Coreano- &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="77f51-128">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77f51-129">Português-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="77f51-129">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77f51-130">Russo –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="77f51-130">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77f51-131">Espanhol-espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="77f51-131">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="77f51-132">O DevTools corresponde automaticamente ao idioma usado para o Microsoft Edge `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="77f51-132">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="77f51-133">Se quiser que o Microsoft Edge esteja em um idioma e seu DevTools permaneça em inglês, pressione `F1` na devtools para abrir [as configurações][Settings] e desabilitar o **idioma do navegador correspondente**.</span><span class="sxs-lookup"><span data-stu-id="77f51-133">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

> ##### <span data-ttu-id="77f51-134">Figura 2</span><span class="sxs-lookup"><span data-stu-id="77f51-134">Figure 2</span></span>  
> <span data-ttu-id="77f51-135">O DevTools em alemão</span><span class="sxs-lookup"><span data-stu-id="77f51-135">The DevTools in German</span></span>  
> ![O DevTools em alemão][ImageLocalizedGerman]  

<span data-ttu-id="77f51-137">As mensagens do **console** não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="77f51-137">**Console** messages are not localized.</span></span>  <span data-ttu-id="77f51-138">Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma usado para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="77f51-138">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="77f51-139">Se você quiser usar o DevTools em um idioma diferente daqueles que estão disponíveis, [tweet][PostTweetEdgeDevTools] conosco ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="77f51-139">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="77f51-140">Chromium problema [#941561][crbug941561]</span><span class="sxs-lookup"><span data-stu-id="77f51-140">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="77f51-141">extensão do Microsoft Edge da WebDicas</span><span class="sxs-lookup"><span data-stu-id="77f51-141">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="77f51-142">A extensão WebDicas da Microsoft Edge permite que você examine facilmente sua página da Web e obtenha comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.</span><span class="sxs-lookup"><span data-stu-id="77f51-142">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="77f51-143">Leia mais em [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="77f51-143">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="77f51-144">Figura 3</span><span class="sxs-lookup"><span data-stu-id="77f51-144">Figure 3</span></span>  
> <span data-ttu-id="77f51-145">A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada</span><span class="sxs-lookup"><span data-stu-id="77f51-145">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada][ImageHintsTabWebhintExtension]  

<span data-ttu-id="77f51-147">[Experimente a extensão do navegador da webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="77f51-147">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="77f51-148">Depois de instalar a extensão, abra a DevTools e selecione a guia dicas.  Aqui, execute uma verificação de site personalizável.</span><span class="sxs-lookup"><span data-stu-id="77f51-148">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="77f51-149">Vá para [webhint.Io][WebhintBrowserExtension] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="77f51-149">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="77f51-150">Modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="77f51-150">3D View</span></span>  

<span data-ttu-id="77f51-151">Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do [modelo de objeto de documento \ (dom \)][MDNDocumentObjectModel] ou do contexto de empilhamento de [índice z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="77f51-151">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="77f51-152">Figura 4</span><span class="sxs-lookup"><span data-stu-id="77f51-152">Figure 4</span></span>  
> <span data-ttu-id="77f51-153">O modo de exibição 3D no DevTools</span><span class="sxs-lookup"><span data-stu-id="77f51-153">The 3D View in the DevTools</span></span>  
> ![O modo de exibição 3D no DevTools][Image3DView]  

<span data-ttu-id="77f51-155">Para acessar o modo de exibição 3D, pressione `Ctrl`  +  `Shift`  +  `P` , digite o **modo de exibição 3D** e selecione **Mostrar modo de exibição 3D**.</span><span class="sxs-lookup"><span data-stu-id="77f51-155">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="77f51-156">Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao modo de exibição 3D, portanto, envie-nos seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="77f51-156">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="77f51-157">Chromium problema [#987787][crbug987787]</span><span class="sxs-lookup"><span data-stu-id="77f51-157">Chromium issue [#987787][crbug987787]</span></span>  

### <span data-ttu-id="77f51-158">Extensões de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="77f51-158">Visual Studio Code extensions</span></span>  

<span data-ttu-id="77f51-159">A equipe do DevTools também lançou algumas extensões para o [código do Visual Studio \ (vs Code \)][VisualStudioCode] que permitem que você use o poder do devtools diretamente do seu editor de texto!</span><span class="sxs-lookup"><span data-stu-id="77f51-159">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="77f51-160">Confira as extensões abaixo:</span><span class="sxs-lookup"><span data-stu-id="77f51-160">Check out the extensions below:</span></span>  

#### <span data-ttu-id="77f51-161">Elementos do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="77f51-161">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="77f51-162">Use a ferramenta de elementos de dentro do código VS adicionando os [elementos para Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs extensão de código.</span><span class="sxs-lookup"><span data-stu-id="77f51-162">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="77f51-163">Figura 5</span><span class="sxs-lookup"><span data-stu-id="77f51-163">Figure 5</span></span>  
> <span data-ttu-id="77f51-164">A ferramenta elementos em código VS usando os elementos da extensão do Microsoft Edge ![ a ferramenta elementos em vs Code usando os elementos da extensão do Microsoft Edge][ImageElementsVisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="77f51-164">The Elements tool in VS Code using the Elements for Microsoft Edge extension ![The Elements tool in VS Code using the Elements for Microsoft Edge extension][ImageElementsVisualStudioCode]</span></span>  

<span data-ttu-id="77f51-165">Para obter mais informações, confira [elementos para o Microsoft Edge vs extensão de código][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="77f51-165">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="77f51-166">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="77f51-166">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="77f51-167">Com o [depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs extensão de código, depure o JavaScript executando no Microsoft Edge diretamente de um código vs!</span><span class="sxs-lookup"><span data-stu-id="77f51-167">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="77f51-168">Figura 6</span><span class="sxs-lookup"><span data-stu-id="77f51-168">Figure 6</span></span>  
> <span data-ttu-id="77f51-169">O depurador para extensão do Microsoft Edge no código VS</span><span class="sxs-lookup"><span data-stu-id="77f51-169">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![O depurador para extensão do Microsoft Edge no código VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="77f51-171">Para obter mais informações, confira [como depurar o Microsoft Edge a partir de código vs][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="77f51-171">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="77f51-172">Dica da web</span><span class="sxs-lookup"><span data-stu-id="77f51-172">webhint</span></span>  

<span data-ttu-id="77f51-173">A extensão de código do [webhint][VisualStudioMarketplaceWebhintExtension] vs usa `webhint` para melhorar sua página da Web enquanto você está escrevendo!</span><span class="sxs-lookup"><span data-stu-id="77f51-173">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="77f51-174">Esta extensão executa e relata os diagnósticos nos arquivos do espaço de trabalho com base na `webhint` análise.</span><span class="sxs-lookup"><span data-stu-id="77f51-174">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="77f51-175">Figura 7</span><span class="sxs-lookup"><span data-stu-id="77f51-175">Figure 7</span></span>  
> <span data-ttu-id="77f51-176">A extensão de código do webhint x que analisa um arquivo. TSX no código VS</span><span class="sxs-lookup"><span data-stu-id="77f51-176">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![A extensão de código do webhint x que analisa um arquivo. TSX no código VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="77f51-178">[Saiba mais sobre a extensão de WebDicas de código vs][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="77f51-178">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="77f51-179">Integração do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="77f51-179">Visual Studio integration</span></span>  

<span data-ttu-id="77f51-180">No Visual Studio 2019 versão 16,2 ou posterior, use o depurador do Visual Studio para Depurar JavaScript em execução no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="77f51-180">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="77f51-181">[Baixe o Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="77f51-181">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="77f51-182">Figura 8</span><span class="sxs-lookup"><span data-stu-id="77f51-182">Figure 8</span></span>  
> <span data-ttu-id="77f51-183">O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta</span><span class="sxs-lookup"><span data-stu-id="77f51-183">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="77f51-185">[Saiba mais sobre como depurar o Microsoft Edge do Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="77f51-185">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="77f51-186">Rastrear mensagens do console de prevenção</span><span class="sxs-lookup"><span data-stu-id="77f51-186">Tracking prevention Console messages</span></span>  

<span data-ttu-id="77f51-187">A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você contra acompanhamento de sites que ainda não visitou.</span><span class="sxs-lookup"><span data-stu-id="77f51-187">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="77f51-188">A configuração de prevenção de rastreamento padrão é o modo balanceado, que bloqueia os rastreadores de terceiros e os rastreadores mal-intencionados conhecidos para obter uma experiência que equilibre a compatibilidade com a privacidade e a compatibilidade com a Web.</span><span class="sxs-lookup"><span data-stu-id="77f51-188">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="77f51-189">Para fornecer a você mais informações sobre a compatibilidade de sua página da Web quando determinados rastreadores estão bloqueados, também adicionamos mensagens de aviso no console quando um controlador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="77f51-189">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="77f51-190">Figura 9</span><span class="sxs-lookup"><span data-stu-id="77f51-190">Figure 9</span></span>  
> <span data-ttu-id="77f51-191">Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador</span><span class="sxs-lookup"><span data-stu-id="77f51-191">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador][ImageTrackingPrevention]  

<span data-ttu-id="77f51-193">[Leia mais sobre a prevenção de rastreamento e o equilíbrio entre a compatibilidade entre privacidade e Web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="77f51-193">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="77f51-194">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="77f51-194">Announcements from the Chromium project</span></span>  

<span data-ttu-id="77f51-195">As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 81 que contribuíram para o projeto de código-fonte aberto Chromium.</span><span class="sxs-lookup"><span data-stu-id="77f51-195">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="77f51-196">Suporte do moto G4 no modo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="77f51-196">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="77f51-197">Depois de [habilitar a barra de ferramentas do dispositivo][DeviceToolbar], simule as dimensões de um visor moto G4 da lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="77f51-197">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

> ##### <span data-ttu-id="77f51-198">Figura 10</span><span class="sxs-lookup"><span data-stu-id="77f51-198">Figure 10</span></span>  
> <span data-ttu-id="77f51-199">Simulando um visor moto G4</span><span class="sxs-lookup"><span data-stu-id="77f51-199">Simulating a Moto G4 viewport</span></span>  
> ![Simulando um visor moto G4][ImageMotoG4]  

<span data-ttu-id="77f51-201">Clique em [Mostrar quadro de dispositivo][DeviceFrame] para mostrar o hardware moto G4 em torno do visor.</span><span class="sxs-lookup"><span data-stu-id="77f51-201">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

> ##### <span data-ttu-id="77f51-202">Figura 11</span><span class="sxs-lookup"><span data-stu-id="77f51-202">Figure 11</span></span>  
> <span data-ttu-id="77f51-203">Mostrando o hardware moto G4</span><span class="sxs-lookup"><span data-stu-id="77f51-203">Showing the Moto G4 hardware</span></span>  
> ![Mostrando o hardware moto G4][ImageMotoG4Frame]  

<span data-ttu-id="77f51-205">Recursos relacionados:</span><span class="sxs-lookup"><span data-stu-id="77f51-205">Related features:</span></span>  

*   <span data-ttu-id="77f51-206">Abra o [menu de comando][CommandMenu] e execute o `Capture screenshot` comando para fazer uma captura de tela do visor que inclua o hardware moto G4 (após habilitar a **exibição do quadro de dispositivo**).</span><span class="sxs-lookup"><span data-stu-id="77f51-206">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="77f51-207">[Acelera a rede e a CPU][ThrottleNetworkAndCpu] para simular com mais precisão as condições de navegação de um usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="77f51-207">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="77f51-208">Chromium problema [#924693][crbug924693]</span><span class="sxs-lookup"><span data-stu-id="77f51-208">Chromium issue [#924693][crbug924693]</span></span>  

### <span data-ttu-id="77f51-209">Atualizações relacionadas a cookies</span><span class="sxs-lookup"><span data-stu-id="77f51-209">Cookie-related updates</span></span>  

#### <span data-ttu-id="77f51-210">Cookies bloqueados no painel cookies</span><span class="sxs-lookup"><span data-stu-id="77f51-210">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="77f51-211">O painel cookies no painel de aplicativos agora exibe cookies bloqueados com um plano de fundo amarelo.</span><span class="sxs-lookup"><span data-stu-id="77f51-211">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

> ##### <span data-ttu-id="77f51-212">Figura 12</span><span class="sxs-lookup"><span data-stu-id="77f51-212">Figure 12</span></span>  
> <span data-ttu-id="77f51-213">Cookies bloqueados no painel cookies do painel do aplicativo</span><span class="sxs-lookup"><span data-stu-id="77f51-213">Blocked cookies in the Cookies pane of the Application panel</span></span>  
> ![Cookies bloqueados no painel cookies do painel do aplicativo][ImageBlockedCookies]  

<span data-ttu-id="77f51-215">Chromium problema [#1030258][crbug|::ref1::|]</span><span class="sxs-lookup"><span data-stu-id="77f51-215">Chromium issue [#1030258][crbug|::ref1::|]</span></span>  

#### <span data-ttu-id="77f51-216">Prioridade do cookie no painel cookies</span><span class="sxs-lookup"><span data-stu-id="77f51-216">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="77f51-217">As tabelas de cookies nos painéis rede e aplicativo agora incluem uma coluna de **prioridade** .</span><span class="sxs-lookup"><span data-stu-id="77f51-217">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="77f51-218">Navegadores baseados em Chromium, como o Microsoft Edge, são os únicos navegadores que dão suporte à prioridade de cookies.</span><span class="sxs-lookup"><span data-stu-id="77f51-218">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="77f51-219">Chromium problema [#1026879][crbug1026879]</span><span class="sxs-lookup"><span data-stu-id="77f51-219">Chromium issue [#1026879][crbug1026879]</span></span>  

#### <span data-ttu-id="77f51-220">Editar todos os valores de cookies</span><span class="sxs-lookup"><span data-stu-id="77f51-220">Edit all cookie values</span></span>  

<span data-ttu-id="77f51-221">Todas as células nas tabelas de cookies são editáveis agora, exceto as células na coluna **tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.</span><span class="sxs-lookup"><span data-stu-id="77f51-221">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="77f51-222">Veja os [campos][CookiesFields] para obter uma explicação de cada coluna.</span><span class="sxs-lookup"><span data-stu-id="77f51-222">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

> ##### <span data-ttu-id="77f51-223">Figura 13</span><span class="sxs-lookup"><span data-stu-id="77f51-223">Figure 13</span></span>  
> <span data-ttu-id="77f51-224">Editando um valor de cookie</span><span class="sxs-lookup"><span data-stu-id="77f51-224">Editing a cookie value</span></span>  
> ![Editando um valor de cookie][ImageEditCookie]  

#### <span data-ttu-id="77f51-226">Copiar como Node.js FETCH para incluir dados de cookies</span><span class="sxs-lookup"><span data-stu-id="77f51-226">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="77f51-227">Clique com o botão direito do mouse em uma solicitação de rede e selecione **copiar**  >  **cópia como Node.js FETCH** para obter uma `fetch` expressão que inclua dados de cookies.</span><span class="sxs-lookup"><span data-stu-id="77f51-227">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

> ##### <span data-ttu-id="77f51-228">Figura 14</span><span class="sxs-lookup"><span data-stu-id="77f51-228">Figure 14</span></span>  
> <span data-ttu-id="77f51-229">Copiar como Node.js Fetch</span><span class="sxs-lookup"><span data-stu-id="77f51-229">Copy as Node.js fetch</span></span>  
> ![Copiar como Node.js Fetch][ImageCopyFetch]  

<span data-ttu-id="77f51-231">Chromium problema [#1029826][crbug1029826]</span><span class="sxs-lookup"><span data-stu-id="77f51-231">Chromium issue [#1029826][crbug1029826]</span></span>  

### <span data-ttu-id="77f51-232">Ícones mais precisos de manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="77f51-232">More accurate web app manifest icons</span></span>  

<span data-ttu-id="77f51-233">Anteriormente, o painel de manifesto no painel do aplicativo enviou suas próprias solicitações para exibir os ícones de manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="77f51-233">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="77f51-234">O DevTools agora mostra o mesmo ícone de manifesto usado pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="77f51-234">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

> ##### <span data-ttu-id="77f51-235">Figura 15</span><span class="sxs-lookup"><span data-stu-id="77f51-235">Figure 15</span></span>  
> <span data-ttu-id="77f51-236">Ícones no painel manifestar</span><span class="sxs-lookup"><span data-stu-id="77f51-236">Icons in the Manifest pane</span></span>  
> ![Ícones no painel manifestar][ImageManifestIcon]  

<span data-ttu-id="77f51-238">Chromium problema [#985402][crbug985402]</span><span class="sxs-lookup"><span data-stu-id="77f51-238">Chromium issue [#985402][crbug985402]</span></span>  

### <span data-ttu-id="77f51-239">Passe o mouse sobre as propriedades do conteúdo CSS para ver os valores sem escape</span><span class="sxs-lookup"><span data-stu-id="77f51-239">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="77f51-240">Passe o mouse sobre o valor de uma `content` propriedade para ver a versão sem escape do valor.</span><span class="sxs-lookup"><span data-stu-id="77f51-240">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="77f51-241">Por exemplo, nesta [demonstração][CSSContentDemo] ao inspecionar o `p::after` pseudo elemento, você vê uma cadeia de caracteres de escape no painel estilos:</span><span class="sxs-lookup"><span data-stu-id="77f51-241">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

> ##### <span data-ttu-id="77f51-242">Figura 16</span><span class="sxs-lookup"><span data-stu-id="77f51-242">Figure 16</span></span>  
> <span data-ttu-id="77f51-243">A cadeia de caracteres de escape</span><span class="sxs-lookup"><span data-stu-id="77f51-243">The escaped string</span></span>  
> ![A cadeia de caracteres de escape][ImageEscapedString]  

<span data-ttu-id="77f51-245">Ao passar o mouse sobre o `content` valor, você vê o valor indesejado:</span><span class="sxs-lookup"><span data-stu-id="77f51-245">When you hover over the `content` value you see the unescaped value:</span></span>  

> ##### <span data-ttu-id="77f51-246">Figura 17</span><span class="sxs-lookup"><span data-stu-id="77f51-246">Figure 17</span></span>  
> <span data-ttu-id="77f51-247">O valor não-escape</span><span class="sxs-lookup"><span data-stu-id="77f51-247">The unescaped value</span></span>  
> ![O valor não-escape][ImageUnescapedString]  

### <span data-ttu-id="77f51-249">Erros de mapa de origem mais detalhados no console</span><span class="sxs-lookup"><span data-stu-id="77f51-249">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="77f51-250">Agora, o console fornece mais detalhes sobre o motivo pelo qual um mapa de origem falhou ao carregar ou analisar.</span><span class="sxs-lookup"><span data-stu-id="77f51-250">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="77f51-251">Anteriormente, era fornecido um erro sem explicar o que aconteceu de errado.</span><span class="sxs-lookup"><span data-stu-id="77f51-251">Previously it just provided an error without explaining what went wrong.</span></span>  

> ##### <span data-ttu-id="77f51-252">Figura 18</span><span class="sxs-lookup"><span data-stu-id="77f51-252">Figure 18</span></span>  
> <span data-ttu-id="77f51-253">Um erro de carregamento do mapa de origem no console</span><span class="sxs-lookup"><span data-stu-id="77f51-253">A source map loading error in the Console</span></span>  
> ![Um erro de carregamento do mapa de origem no console][ImageSourcemapError]  

### <span data-ttu-id="77f51-255">Configuração para desativar a rolagem após o final de um arquivo</span><span class="sxs-lookup"><span data-stu-id="77f51-255">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="77f51-256">Abra [configurações][Settings] e, em **Preferences**seguida, desabilite as  >  **fontes**  >  **de preferências permitem a rolagem do final do arquivo** para desativar o comportamento padrão da interface do usuário que permite rolar bem após o final de um arquivo no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="77f51-256">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

> ##### <span data-ttu-id="77f51-257">Figura 19</span><span class="sxs-lookup"><span data-stu-id="77f51-257">Figure 19</span></span>  
> <span data-ttu-id="77f51-258">Desativando **permitir rolagem após o fim do arquivo** em configurações</span><span class="sxs-lookup"><span data-stu-id="77f51-258">Disabling **Allow scrolling past end of file** in Settings</span></span>  
> ![Desativando permitir rolagem após o final do arquivo][ImageSettings]  

> ##### <span data-ttu-id="77f51-260">Figura 20</span><span class="sxs-lookup"><span data-stu-id="77f51-260">Figure 20</span></span>  
> <span data-ttu-id="77f51-261">A rolagem após o final de um arquivo agora está desabilitada no painel fontes</span><span class="sxs-lookup"><span data-stu-id="77f51-261">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
> ![A rolagem após o final de um arquivo agora está desabilitada no painel fontes][ImageScroll]  

## <span data-ttu-id="77f51-263">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="77f51-263">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="77f51-264">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="77f51-264">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="77f51-265">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="77f51-265">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="77f51-266">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="77f51-266">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Figura 1: a ferramenta de desempenho no DevTools com as melhorias de navegação do teclado e do leitor de tela"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Figura 2: o DevTools em alemão"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Figura 3: a guia dicas no Microsoft Edge DevTools quando a extensão do navegador webhints está instalada"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Figura 4: modo de exibição 3D no Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Figura 5: a ferramenta elementos no código VS usando os elementos da extensão do Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Figura 6: o depurador para extensão do Microsoft Edge no código VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Figura 7: a extensão de código do webhint x que analisa arquivos. TSX no código VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Figura 8: Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Figura 9: mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Figura 10: simulando um visor moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Figura 11: mostrando o hardware moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Figura 12: cookies bloqueados no painel cookies do painel do aplicativo"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Figura 13: editando um valor de cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Figura 14: copiar como Node.js Fetch"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Figura 15: ícones no painel de manifesto"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Figura 16: a cadeia de caracteres de escape"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Figura 17: o valor não-escape"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Figura 18: um erro de carregamento do mapa de origem no console"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Figura 19: desativando permitir rolagem após o fim do arquivo em configurações"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Figura 20: rolar após o final de um arquivo agora está desabilitado no painel fontes"

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular um visor móvel com o modo de dispositivo no Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Selecione Mostrar quadro de dispositivo para mostrar a estrutura do dispositivo físico em torno do visor."
[CommandMenu]: ../../../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limite a rede e a CPU para simular com mais precisão as condições de navegação de um usuário móvel."
[crbug924693]: https://crbug.com/924693 "924693: solicitação de recurso: Adicionar moto G4 à lista de modo de dispositivo"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: a guia cookies no console de desenvolvimento não mostra mais prioridade"
[CookiesFields]: ../../../storage/cookies.md#fields "Os campos na tabela de cookies"
[crbug1029826]: https://crbug.com/1029826 "1029826: guia rede-> clique com o botão direito do mouse para solicitar-> copiar-> copiar como busca não copiar cookies"
[crbug985402]: https://crbug.com/985402 "985402: o erro do ícone do manifesto do aplicativo Web cadeia de caracteres de erro é confuso"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração de conteúdo CSS não escape"
[Settings]: ../../../customize/index.md#settings "Personalizar o Microsoft Edge DevTools com configurações"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para extensão de código do Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos da extensão de código do Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools não são compatíveis com a WCAG"
[crbug941561]: https://crbug.com/941561 "941561-localização da DevTools"
[crbug987787]: https://crbug.com/987787 "987787-modo de exibição 3D dom"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Informações sobre acessibilidade"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos do Microsoft Edge Insider"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixe o Visual Studio 2019 para Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (modelo de objeto de documento) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-índice | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Código do Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \ (Chromium \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensão do navegador webhint | documentação do webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint VS extensão de código | documentação do webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem de blog do Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="77f51-323">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="77f51-323">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="77f51-324">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/01/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="77f51-324">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="77f51-326">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="77f51-326">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  