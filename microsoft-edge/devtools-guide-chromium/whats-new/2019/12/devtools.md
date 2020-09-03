---
description: Melhorias de acessibilidade, uso de DevTools em outros idiomas e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: dcc6c97cfb355d654c596f4be29de6507174bebd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993398"
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

# <span data-ttu-id="0f889-104">O que há de novo no DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="0f889-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <span data-ttu-id="0f889-105">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0f889-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="0f889-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="0f889-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="0f889-107">Dê uma olhada neles para experimentar os novos recursos do DevTools, as extensões de código do VS e muito mais.</span><span class="sxs-lookup"><span data-stu-id="0f889-107">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="0f889-108">Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="0f889-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="0f889-109">Melhorias de acessibilidade no DevTools</span><span class="sxs-lookup"><span data-stu-id="0f889-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="0f889-110">A equipe do DevTools contribuiu com as mudanças do 170 para o Chromium para solucionar problemas de cor de alto impacto, teclado e leitor de tela no DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f889-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="0f889-111">Cada desenvolvedor que cria a Web deve poder usar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f889-111">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="0f889-112">Figura 1</span><span class="sxs-lookup"><span data-stu-id="0f889-112">Figure 1</span></span>  
> <span data-ttu-id="0f889-113">A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela</span><span class="sxs-lookup"><span data-stu-id="0f889-113">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="0f889-115">Deseja saber como tornar sua página da Web acessível a todos os seus usuários?</span><span class="sxs-lookup"><span data-stu-id="0f889-115">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="0f889-116">Baixe as [informações sobre acessibilidade][AccessibilityInsights] e as extensões [webhint][WebhintBrowserExtension] para o Microsoft Edge para começar.</span><span class="sxs-lookup"><span data-stu-id="0f889-116">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="0f889-117">Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="0f889-117">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0f889-118">Chromium problema [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="0f889-118">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="0f889-119">Usando o DevTools em outros idiomas</span><span class="sxs-lookup"><span data-stu-id="0f889-119">Using the DevTools in other languages</span></span>  

<span data-ttu-id="0f889-120">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e código VS, em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="0f889-120">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="0f889-121">Estamos entusiasmados a anunciar a localização do DevTools, que agora você pode usar em um dos dez idiomas além do inglês:</span><span class="sxs-lookup"><span data-stu-id="0f889-121">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="0f889-122">Chinês \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="0f889-122">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0f889-123">Chinês \ (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="0f889-123">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0f889-124">Francês – Fran-Fran&#231;ais</span><span class="sxs-lookup"><span data-stu-id="0f889-124">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0f889-125">Alemão – Deutsch</span><span class="sxs-lookup"><span data-stu-id="0f889-125">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0f889-126">Italiano-Italiano</span><span class="sxs-lookup"><span data-stu-id="0f889-126">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0f889-127"> &#26085;&#26412;&#35486; japonês</span><span class="sxs-lookup"><span data-stu-id="0f889-127">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0f889-128">Coreano- &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="0f889-128">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0f889-129">Português-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="0f889-129">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0f889-130">Russo –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="0f889-130">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0f889-131">Espanhol-espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="0f889-131">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="0f889-132">Navegue até `edge://flags` e defina o sinalizador **habilitar ferramentas para desenvolvedores localizados** como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="0f889-132">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="0f889-133">Defina também o sinalizador de **experimentos das ferramentas de desenvolvedor** como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="0f889-133">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="0f889-134">Reinicie o Microsoft Edge e abra o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f889-134">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="0f889-135">O DevTools corresponde ao idioma usado para o Microsoft Edge `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="0f889-135">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

> ##### <span data-ttu-id="0f889-136">Figura 2</span><span class="sxs-lookup"><span data-stu-id="0f889-136">Figure 2</span></span>  
> <span data-ttu-id="0f889-137">O DevTools em alemão</span><span class="sxs-lookup"><span data-stu-id="0f889-137">The DevTools in German</span></span>  
> ![O DevTools em alemão][ImageLocalizedGerman]  

<span data-ttu-id="0f889-139">Se você quiser usar o DevTools em um idioma diferente daqueles que estão disponíveis, [tweet][PostTweetEdgeDevTools] conosco ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="0f889-139">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="0f889-140">Chromium problema [#941561][crbug941561]</span><span class="sxs-lookup"><span data-stu-id="0f889-140">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="0f889-141">extensão do Microsoft Edge da WebDicas</span><span class="sxs-lookup"><span data-stu-id="0f889-141">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="0f889-142">A extensão WebDicas da Microsoft Edge permite que você examine facilmente sua página da Web e obtenha comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f889-142">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="0f889-143">Leia mais em [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="0f889-143">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="0f889-144">Figura 3</span><span class="sxs-lookup"><span data-stu-id="0f889-144">Figure 3</span></span>  
> <span data-ttu-id="0f889-145">A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada</span><span class="sxs-lookup"><span data-stu-id="0f889-145">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada][ImageHintsTabWebhintExtension]  

<span data-ttu-id="0f889-147">[Experimente a extensão do navegador da webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="0f889-147">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="0f889-148">Depois de instalar a extensão, abra a DevTools e selecione a guia dicas.  Aqui, execute uma verificação de site personalizável.</span><span class="sxs-lookup"><span data-stu-id="0f889-148">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="0f889-149">Vá para [webhint.Io][WebhintBrowserExtension] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="0f889-149">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="0f889-150">Modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="0f889-150">3D View</span></span>  

<span data-ttu-id="0f889-151">Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do [modelo de objeto de documento \ (dom \)][MDNDocumentObjectModel] ou do contexto de empilhamento de [índice z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="0f889-151">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="0f889-152">Figura 4</span><span class="sxs-lookup"><span data-stu-id="0f889-152">Figure 4</span></span>  
> <span data-ttu-id="0f889-153">O modo de exibição 3D no DevTools</span><span class="sxs-lookup"><span data-stu-id="0f889-153">The 3D View in the DevTools</span></span>  
> ![O modo de exibição 3D no DevTools][Image3DView]  

<span data-ttu-id="0f889-155">Para acessar o modo de exibição 3D, navegue até `edge://flags` e assegure-se de que o sinalizador de **experimentos das ferramentas de desenvolvedor** esteja definido como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="0f889-155">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="0f889-156">Reinicie o Microsoft Edge e abra o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f889-156">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="0f889-157">Pressione `F1` na seção devtools ou vá para **configurações**, navegue até **experimentos** e marque a caixa de seleção **habilitar modo de exibição 3D** .</span><span class="sxs-lookup"><span data-stu-id="0f889-157">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="0f889-158">Agora, pressione `Ctrl`  +  `Shift`  +  `P` , digite o **modo de exibição 3D** e selecione **Mostrar modo de exibição 3D**.</span><span class="sxs-lookup"><span data-stu-id="0f889-158">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="0f889-159">Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao modo de exibição 3D para nos enviar seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="0f889-159">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="0f889-160">Chromium problema [#987787][crbug987787]</span><span class="sxs-lookup"><span data-stu-id="0f889-160">Chromium issue [#987787][crbug987787]</span></span>

### <span data-ttu-id="0f889-161">Extensões de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0f889-161">Visual Studio Code extensions</span></span>  

<span data-ttu-id="0f889-162">A equipe do DevTools também lançou algumas extensões para o [código do Visual Studio \ (vs Code \)][VisualStudioCode] que permitem que você use o poder do devtools diretamente do seu editor de texto!</span><span class="sxs-lookup"><span data-stu-id="0f889-162">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="0f889-163">Confira as extensões abaixo:</span><span class="sxs-lookup"><span data-stu-id="0f889-163">Check out the extensions below:</span></span>  

#### <span data-ttu-id="0f889-164">Elementos do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f889-164">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="0f889-165">Use a ferramenta de elementos de dentro do código VS adicionando os [elementos para Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs extensão de código.</span><span class="sxs-lookup"><span data-stu-id="0f889-165">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="0f889-166">Figura 5</span><span class="sxs-lookup"><span data-stu-id="0f889-166">Figure 5</span></span>  
> <span data-ttu-id="0f889-167">A ferramenta elementos no código VS usando os elementos da extensão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f889-167">The Elements tool in VS Code using the Elements for Microsoft Edge extension</span></span>  
> ![A ferramenta elementos no código VS usando os elementos da extensão do Microsoft Edge][ImageElementsVisualStudioCode]  

<span data-ttu-id="0f889-169">Para obter mais informações, confira [elementos para o Microsoft Edge vs extensão de código][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="0f889-169">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="0f889-170">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f889-170">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="0f889-171">Com o [depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs extensão de código, depure o JavaScript executando no Microsoft Edge diretamente de um código vs!</span><span class="sxs-lookup"><span data-stu-id="0f889-171">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="0f889-172">Figura 6</span><span class="sxs-lookup"><span data-stu-id="0f889-172">Figure 6</span></span>  
> <span data-ttu-id="0f889-173">O depurador para extensão do Microsoft Edge no código VS</span><span class="sxs-lookup"><span data-stu-id="0f889-173">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![O depurador para extensão do Microsoft Edge no código VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="0f889-175">Para obter mais informações, confira [como depurar o Microsoft Edge a partir de código vs][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="0f889-175">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="0f889-176">Dica da web</span><span class="sxs-lookup"><span data-stu-id="0f889-176">webhint</span></span>  

<span data-ttu-id="0f889-177">A extensão de código do [webhint][VisualStudioMarketplaceWebhintExtension] vs usa `webhint` para melhorar sua página da Web enquanto você está escrevendo!</span><span class="sxs-lookup"><span data-stu-id="0f889-177">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="0f889-178">Esta extensão executa e relata os diagnósticos nos arquivos do espaço de trabalho com base na `webhint` análise.</span><span class="sxs-lookup"><span data-stu-id="0f889-178">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="0f889-179">Figura 7</span><span class="sxs-lookup"><span data-stu-id="0f889-179">Figure 7</span></span>  
> <span data-ttu-id="0f889-180">A extensão de código do webhint x que analisa um arquivo. TSX no código VS</span><span class="sxs-lookup"><span data-stu-id="0f889-180">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![A extensão de código do webhint x que analisa um arquivo. TSX no código VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="0f889-182">[Saiba mais sobre a extensão de WebDicas de código vs][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="0f889-182">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="0f889-183">Integração do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0f889-183">Visual Studio integration</span></span>
<span data-ttu-id="0f889-184">No Visual Studio 2019 versão 16,2 ou posterior, use o depurador do Visual Studio para Depurar JavaScript em execução no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f889-184">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="0f889-185">[Baixe o Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="0f889-185">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="0f889-186">Figura 8</span><span class="sxs-lookup"><span data-stu-id="0f889-186">Figure 8</span></span>  
> <span data-ttu-id="0f889-187">O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta</span><span class="sxs-lookup"><span data-stu-id="0f889-187">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="0f889-189">[Leia nossa postagem no blog para saber como depurar o Microsoft Edge do Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="0f889-189">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="0f889-190">Rastrear mensagens do console de prevenção</span><span class="sxs-lookup"><span data-stu-id="0f889-190">Tracking prevention Console messages</span></span>  

<span data-ttu-id="0f889-191">A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você contra acompanhamento de sites que ainda não visitou.</span><span class="sxs-lookup"><span data-stu-id="0f889-191">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="0f889-192">A configuração de prevenção de rastreamento padrão é o modo balanceado, que bloqueia os rastreadores de terceiros e os rastreadores mal-intencionados conhecidos para obter uma experiência que equilibre a compatibilidade com a privacidade e a compatibilidade com a Web.</span><span class="sxs-lookup"><span data-stu-id="0f889-192">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="0f889-193">Para fornecer a você mais informações sobre a compatibilidade de sua página da Web quando determinados rastreadores estão bloqueados, também adicionamos mensagens de aviso no console quando um controlador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0f889-193">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="0f889-194">Figura 9</span><span class="sxs-lookup"><span data-stu-id="0f889-194">Figure 9</span></span>  
> <span data-ttu-id="0f889-195">Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador</span><span class="sxs-lookup"><span data-stu-id="0f889-195">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador][ImageTrackingPrevention]  

<span data-ttu-id="0f889-197">[Leia mais sobre a prevenção de rastreamento e o equilíbrio entre a compatibilidade entre privacidade e Web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="0f889-197">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="0f889-198">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="0f889-198">Announcements from the Chromium project</span></span>  

<span data-ttu-id="0f889-199">As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 80 que contribuíram para o projeto de código-fonte aberto Chromium.</span><span class="sxs-lookup"><span data-stu-id="0f889-199">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="0f889-200">Suporte a redeclaraçãos Let e Class no console</span><span class="sxs-lookup"><span data-stu-id="0f889-200">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="0f889-201">O console agora oferece suporte a redeclarações `let` e `class` instruções.</span><span class="sxs-lookup"><span data-stu-id="0f889-201">The Console now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="0f889-202">A incapacidade de redeclarar foi um aborrecimento comum para desenvolvedores da Web que usam o console para experimentar com o novo código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0f889-202">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="0f889-203">A redeclaração de uma `let` `class` instrução ou de uma instrução em um script fora do console ou dentro de uma única entrada de console ainda causa uma `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="0f889-203">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="0f889-204">Por exemplo, anteriormente, ao redeclarar uma variável local com `let` , o console emitiu um erro:</span><span class="sxs-lookup"><span data-stu-id="0f889-204">For example, previously, when redeclaring a local variable with `let`, the Console threw an error:</span></span>  

> ##### <span data-ttu-id="0f889-205">Figura 10</span><span class="sxs-lookup"><span data-stu-id="0f889-205">Figure 10</span></span>  
> <span data-ttu-id="0f889-206">O console no Microsoft Edge 79 mostrando que a redeclaração Let falha</span><span class="sxs-lookup"><span data-stu-id="0f889-206">The Console in Microsoft Edge 79 showing that the let redeclaration fails</span></span>  
> ![O console no Microsoft Edge 79 mostrando que a redeclaração Let falha][ImageConsoleRedeclarationFails]  

<span data-ttu-id="0f889-208">Agora, o console permite a redeclaração:</span><span class="sxs-lookup"><span data-stu-id="0f889-208">Now, the Console allows the redeclaration:</span></span>  

> ##### <span data-ttu-id="0f889-209">Figura 11</span><span class="sxs-lookup"><span data-stu-id="0f889-209">Figure 11</span></span>  
> <span data-ttu-id="0f889-210">O console no Microsoft Edge 80 mostrando que a redeclaração permite que a redeclaração seja bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="0f889-210">The Console in Microsoft Edge 80 showing that the let redeclaration succeeds</span></span>  
> ![O console no Microsoft Edge 80 mostrando que a redeclaração permite que a redeclaração seja bem-sucedida][ImageConsoleRedeclarationSucceeds]  

<span data-ttu-id="0f889-212">Chromium problema [#1004193][crbug1004193]</span><span class="sxs-lookup"><span data-stu-id="0f889-212">Chromium issue [#1004193][crbug1004193]</span></span>  

### <span data-ttu-id="0f889-213">Depuração de Webassembly aprimorada</span><span class="sxs-lookup"><span data-stu-id="0f889-213">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="0f889-214">DevTools começou a dar suporte ao [padrão de depuração Dwarf][DwarfHome], o que significa maior suporte para a depuração de código, a definição de pontos de interrupção e a resolução de rastreamentos de pilha em seus idiomas de origem no devtools.</span><span class="sxs-lookup"><span data-stu-id="0f889-214">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### <span data-ttu-id="0f889-215">Atualizações do painel de rede</span><span class="sxs-lookup"><span data-stu-id="0f889-215">Network panel updates</span></span>  

#### <span data-ttu-id="0f889-216">Solicitar cadeias do iniciador na guia iniciador</span><span class="sxs-lookup"><span data-stu-id="0f889-216">Request Initiator Chains in the Initiator tab</span></span>  

<span data-ttu-id="0f889-217">Agora você pode ver os iniciadores e as dependências de uma solicitação de rede como uma lista aninhada.</span><span class="sxs-lookup"><span data-stu-id="0f889-217">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="0f889-218">Isso pode ajudá-lo a entender por que um recurso foi solicitado ou de qual atividade de rede um determinado recurso \ (por exemplo, um script \) causou.</span><span class="sxs-lookup"><span data-stu-id="0f889-218">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

> ##### <span data-ttu-id="0f889-219">Figura 12</span><span class="sxs-lookup"><span data-stu-id="0f889-219">Figure 12</span></span>  
> <span data-ttu-id="0f889-220">Uma cadeia de iniciador de solicitações na guia iniciador</span><span class="sxs-lookup"><span data-stu-id="0f889-220">A Request Initiator Chain in the Initiator tab</span></span>  
> ![Uma cadeia de iniciador de solicitações na guia iniciador][ImageRequestInitiatorChain]  

<span data-ttu-id="0f889-222">Depois de [registrar a atividade de rede no painel de rede][DevToolsNetworkIndex], clique em um recurso e, em seguida, vá para a guia **iniciador** para ver a **cadeia do iniciador de solicitações**:</span><span class="sxs-lookup"><span data-stu-id="0f889-222">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="0f889-223">O **recurso inspecionado** está em negrito.</span><span class="sxs-lookup"><span data-stu-id="0f889-223">The **inspected resource** is bold.</span></span>  <span data-ttu-id="0f889-224">Na captura de tela acima, `ai.2.min.js` é o recurso inspecionado.</span><span class="sxs-lookup"><span data-stu-id="0f889-224">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="0f889-225">Os recursos acima do recurso inspecionado são os **iniciadores**.</span><span class="sxs-lookup"><span data-stu-id="0f889-225">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="0f889-226">Na captura de tela acima, `https://www.microsoftedgeinsider.com` é o iniciador de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0f889-226">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="0f889-227">Em outras palavras, `https://www.microsoftedgeinsider.com` causou a solicitação de rede `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0f889-227">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="0f889-228">Os recursos abaixo do recurso inspecionado são as **dependências**.</span><span class="sxs-lookup"><span data-stu-id="0f889-228">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="0f889-229">Na captura de tela acima, `https://dc.services.visualstudio.com/v2/track` é uma dependência de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0f889-229">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="0f889-230">Em outras palavras, `ai.2.min.js` causou a solicitação de rede `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="0f889-230">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="0f889-231">As informações de dependência e de iniciador também podem ser acessadas mantendo `Shift` e passando o mouse sobre os recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="0f889-231">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="0f889-232">Consulte [Exibir iniciadores e dependências][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="0f889-232">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="0f889-233">Chromium problema [#842488][crbug842488]</span><span class="sxs-lookup"><span data-stu-id="0f889-233">Chromium issue [#842488][crbug842488]</span></span>  

#### <span data-ttu-id="0f889-234">Realçar a solicitação de rede selecionada na visão geral</span><span class="sxs-lookup"><span data-stu-id="0f889-234">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="0f889-235">Depois de clicar em um recurso de rede para inspecioná-lo, o painel de rede agora coloca uma borda azul ao meio do recurso na **visão geral**.</span><span class="sxs-lookup"><span data-stu-id="0f889-235">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="0f889-236">Isso pode ajudá-lo a detectar se a solicitação de rede está acontecendo antes ou depois do esperado.</span><span class="sxs-lookup"><span data-stu-id="0f889-236">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

> ##### <span data-ttu-id="0f889-237">Figura 13</span><span class="sxs-lookup"><span data-stu-id="0f889-237">Figure 13</span></span>  
> <span data-ttu-id="0f889-238">O painel Visão geral destacando o recurso inspecionado</span><span class="sxs-lookup"><span data-stu-id="0f889-238">The Overview pane highlighting the inspected resource</span></span>  
> ![O painel Visão geral destacando o recurso inspecionado][ImageOverviewPaneInspectedResource]  

<span data-ttu-id="0f889-240">Chromium problema [#988253][crbug988253]</span><span class="sxs-lookup"><span data-stu-id="0f889-240">Chromium issue [#988253][crbug988253]</span></span>  

#### <span data-ttu-id="0f889-241">Colunas URL e caminho no painel rede</span><span class="sxs-lookup"><span data-stu-id="0f889-241">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="0f889-242">Use as colunas novo **caminho** e **URL** no painel **rede** para ver o caminho absoluto ou a URL completa de cada recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="0f889-242">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

> ##### <span data-ttu-id="0f889-243">Figura 14</span><span class="sxs-lookup"><span data-stu-id="0f889-243">Figure 14</span></span>  
> <span data-ttu-id="0f889-244">As colunas novo caminho e URL no painel de rede</span><span class="sxs-lookup"><span data-stu-id="0f889-244">The new Path and URL columns in the Network panel</span></span>  
> ![As colunas novo caminho e URL no painel de rede][ImagePathNetworkPanel]  

<span data-ttu-id="0f889-246">Clique com o botão direito do mouse no cabeçalho da tabela de **cascata** e selecione **caminho** ou **URL** para mostrar as novas colunas.</span><span class="sxs-lookup"><span data-stu-id="0f889-246">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="0f889-247">Chromium problema [#993366][crbug993366]</span><span class="sxs-lookup"><span data-stu-id="0f889-247">Chromium issue [#993366][crbug993366]</span></span>  

#### <span data-ttu-id="0f889-248">Cadeias de agente do usuário atualizadas</span><span class="sxs-lookup"><span data-stu-id="0f889-248">Updated User-Agent strings</span></span>  

<span data-ttu-id="0f889-249">O DevTools dá suporte à configuração de uma cadeia de caracteres de agente de usuário personalizada por meio da guia **condições de rede** .  A cadeia de caracteres do agente do usuário afeta o `User-Agent` cabeçalho http anexado aos recursos de rede e também o valor de `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="0f889-249">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="0f889-250">As cadeias de caracteres de agente do usuário predefinidos foram atualizadas para refletir versões modernas do navegador.</span><span class="sxs-lookup"><span data-stu-id="0f889-250">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

> ##### <span data-ttu-id="0f889-251">Figura 15</span><span class="sxs-lookup"><span data-stu-id="0f889-251">Figure 15</span></span>  
> <span data-ttu-id="0f889-252">O menu do agente do usuário na guia condições de rede</span><span class="sxs-lookup"><span data-stu-id="0f889-252">The User Agent menu in the Network Conditions tab</span></span>  
> ![O menu do agente do usuário na guia condições de rede][ImageUserAgentNetworkConditionsTab]  

<span data-ttu-id="0f889-254">Para acessar as **condições da rede**, [abra o menu de comando][DevToolsCommandMenuIndex] e execute o `Show Network Conditions` comando.</span><span class="sxs-lookup"><span data-stu-id="0f889-254">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="0f889-255">Você também pode [definir cadeias de caracteres de agente do usuário no modo de dispositivo][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="0f889-255">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="0f889-256">Chromium problema [#1029031][crbug1029031]</span><span class="sxs-lookup"><span data-stu-id="0f889-256">Chromium issue [#1029031][crbug1029031]</span></span>  

### <span data-ttu-id="0f889-257">Atualizações do painel auditorias</span><span class="sxs-lookup"><span data-stu-id="0f889-257">Audits panel updates</span></span>  

#### <span data-ttu-id="0f889-258">Nova interface do usuário de configuração</span><span class="sxs-lookup"><span data-stu-id="0f889-258">New configuration UI</span></span>  

<span data-ttu-id="0f889-259">A interface do usuário de configuração tem um design novo e responsivo, e as opções de configuração de limitação foram simplificadas.</span><span class="sxs-lookup"><span data-stu-id="0f889-259">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="0f889-260">Consulte [limitação do painel de auditoria][GitHubGoogleChromeDevToolsAuditsPanelThrottling] para obter mais informações sobre as alterações na interface do usuário de limitação.</span><span class="sxs-lookup"><span data-stu-id="0f889-260">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

> ##### <span data-ttu-id="0f889-261">Figura 16</span><span class="sxs-lookup"><span data-stu-id="0f889-261">Figure 16</span></span>  
> <span data-ttu-id="0f889-262">A nova interface do usuário de configuração</span><span class="sxs-lookup"><span data-stu-id="0f889-262">The new configuration UI</span></span>  
> ![A nova interface do usuário de configuração][ImageConfigurationUI]  

### <span data-ttu-id="0f889-264">Atualizações da guia cobertura</span><span class="sxs-lookup"><span data-stu-id="0f889-264">Coverage tab updates</span></span>  

#### <span data-ttu-id="0f889-265">Modos de cobertura per-Function ou per-Block</span><span class="sxs-lookup"><span data-stu-id="0f889-265">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="0f889-266">A [guia cobertura][DevToolsCoverageIndex] tem um novo menu suspenso que permite especificar se os dados da cobertura de código devem ser coletados **por função** ou **por bloco**.</span><span class="sxs-lookup"><span data-stu-id="0f889-266">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="0f889-267">A cobertura **por bloco** é mais detalhada, mas também muito mais cara para coletar.</span><span class="sxs-lookup"><span data-stu-id="0f889-267">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="0f889-268">O DevTools usa a cobertura **por função** por padrão agora.</span><span class="sxs-lookup"><span data-stu-id="0f889-268">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="0f889-269">Você pode ver diferenças em grandes coberturas de código em arquivos HTML, dependendo se você usa o modo **por função** ou **por bloqueio** .</span><span class="sxs-lookup"><span data-stu-id="0f889-269">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="0f889-270">Ao usar o modo **por função** , scripts embutidos em arquivos HTML são tratados como funções.</span><span class="sxs-lookup"><span data-stu-id="0f889-270">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="0f889-271">Se o script for executado de forma alguma, o DevTools marcará todo o script como código usado.</span><span class="sxs-lookup"><span data-stu-id="0f889-271">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="0f889-272">Somente se o script não for executado, o DevTools marcará o script como código não usado.</span><span class="sxs-lookup"><span data-stu-id="0f889-272">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

> ##### <span data-ttu-id="0f889-273">Figura 17</span><span class="sxs-lookup"><span data-stu-id="0f889-273">Figure 17</span></span>  
> <span data-ttu-id="0f889-274">O menu suspenso modo de cobertura</span><span class="sxs-lookup"><span data-stu-id="0f889-274">The coverage mode dropdown menu</span></span>  
> ![O menu suspenso modo de cobertura][ImageCoverageMode]  

#### <span data-ttu-id="0f889-276">A cobertura agora deve ser iniciada por uma recarga de página</span><span class="sxs-lookup"><span data-stu-id="0f889-276">Coverage must now be initiated by a page reload</span></span>  

<span data-ttu-id="0f889-277">A alternância da cobertura de código sem um recarregamento de página foi removida porque os dados de cobertura não eram confiáveis.</span><span class="sxs-lookup"><span data-stu-id="0f889-277">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="0f889-278">Por exemplo, uma função pode ser reportada como não usada se o tempo de execução era muito demorado e o coletor de lixo V8 o limpou.</span><span class="sxs-lookup"><span data-stu-id="0f889-278">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="0f889-279">Chromium problema [#1004203][crbug1004203]</span><span class="sxs-lookup"><span data-stu-id="0f889-279">Chromium issue [#1004203][crbug1004203]</span></span>  

## <span data-ttu-id="0f889-280">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f889-280">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="0f889-281">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="0f889-281">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="0f889-282">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f889-282">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="0f889-283">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="0f889-283">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Figura 1: a ferramenta de desempenho no DevTools com as melhorias de navegação do teclado e do leitor de tela"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Figura 2: o DevTools em alemão"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Figura 3: a guia dicas no Microsoft Edge DevTools quando a extensão do navegador webhints está instalada"  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Figura 4: modo de exibição 3D no Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Figura 5: a ferramenta elementos no código VS usando os elementos da extensão do Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Figura 6: o depurador para extensão do Microsoft Edge no código VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Figura 7: a extensão de código do webhint x que analisa arquivos. TSX no código VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Figura 8: Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Figura 9: mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador"  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Figura 10: o console no Microsoft Edge 79 mostrando que a redeclaração Let falha"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "Figura 11: o console no Microsoft Edge 80 mostrando que a redeclaração permite que a redeclaração seja bem-sucedida"  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Figura 12: uma cadeia de iniciador de solicitação na guia iniciador"  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Figura 13: painel Visão geral realçando o recurso inspecionado"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Figura 14: as colunas novo caminho e URL no painel de rede"  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Figura 15: o menu do agente do usuário na guia condições de rede"  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Figura 16: a nova interface do usuário de configuração"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Figura 17: menu suspenso modo de cobertura"  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular um visor móvel-simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Inspecionar atividades de rede no Microsoft Edge DevTools"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Exibir iniciadores e dependências-referência de análise de rede"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Novidades do EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para extensão de código do Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos da extensão de código do Microsoft Edge VS"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488-adicione o campo Initiator à guia cabeçalhos-monorail"  
[crbug988253]: https://crbug.com/988253 "988253-bug DevTools-nenhuma associação entre solicitação de rede e gráfico de linha do tempo-monorail"  
[crbug993366]: https://crbug.com/993366 "993366 – mostra a parte do caminho da URL na lista de solicitações do painel de rede-monorail"  
[crbug1004193]: https://crbug.com/1004193 "1004193-modo de REPL para V8-monorail"  
[crbug1004203]: https://crbug.com/1004203 "1004203-monorail"  
[crbug1029031]: https://crbug.com/1029031 "as cadeias de caracteres do 1029031-UA estão sendo desatualizadas-monorail" 
[crbug963183]: https://crbug.com/963183 "963183-DevTools não são compatíveis com a WCAG"
[crbug941561]: https://crbug.com/941561 "941561-localização da DevTools"
[crbug987787]: https://crbug.com/987787 "987787-modo de exibição 3D dom"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Informações sobre acessibilidade"  

[DwarfHome]: https://dwarfstd.org "Página inicial do Dwarf"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools ' limitação do painel de auditoria-GoogleChrome/Lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos do Microsoft Edge Insider"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Depurar JavaScript no Microsoft Edge do Visual Studio | Blog do Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixe o Visual Studio 2019 para Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (modelo de objeto de documento) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-índice | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Código do Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \ (Chromium \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensão do navegador webhint | documentação do webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint VS extensão de código | documentação do webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem de blog do Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"

> [!NOTE]
> <span data-ttu-id="0f889-340">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="0f889-340">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0f889-341">A página original é encontrada [aqui](https://developers.google.com/web/updates/2019/12/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="0f889-341">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0f889-343">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0f889-343">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
