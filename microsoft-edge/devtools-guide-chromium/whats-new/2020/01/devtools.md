---
description: Modo de exibição 3D, integração do Visual Studio com o Microsoft Edge e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3081ebb256a9ede637aaaddc3c3cdf7a70a201bb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015472"
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

# <span data-ttu-id="5494f-104">O que há de novo no DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="5494f-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="5494f-105">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5494f-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="5494f-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="5494f-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="5494f-107">Dê uma olhada neles para experimentar novos recursos no DevTools, extensões de código do Visual Studio e muito mais.</span><span class="sxs-lookup"><span data-stu-id="5494f-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="5494f-108">Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="5494f-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="5494f-109">Melhorias de acessibilidade no DevTools</span><span class="sxs-lookup"><span data-stu-id="5494f-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="5494f-110">A equipe do DevTools contribuiu com as mudanças do 170 para o Chromium para solucionar problemas de cor de alto impacto, teclado e leitor de tela no DevTools.</span><span class="sxs-lookup"><span data-stu-id="5494f-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="5494f-111">Cada desenvolvedor que cria a Web deve poder usar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="5494f-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="5494f-113">A ferramenta **desempenho** no devtools com melhorias de navegação do teclado e leitor de tela</span><span class="sxs-lookup"><span data-stu-id="5494f-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-114">Deseja saber como tornar sua página da Web acessível a todos os seus usuários?</span><span class="sxs-lookup"><span data-stu-id="5494f-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="5494f-115">Baixe as [informações sobre acessibilidade][AccessibilityInsights] e as extensões [webhint][WebhintBrowserExtension] para o Microsoft Edge para começar.</span><span class="sxs-lookup"><span data-stu-id="5494f-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="5494f-116">Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="5494f-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="5494f-117">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="5494f-117">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="5494f-118">Usando o DevTools em outros idiomas</span><span class="sxs-lookup"><span data-stu-id="5494f-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="5494f-119">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como o código do StackOverflow e do Visual Studio, em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="5494f-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="5494f-120">Estamos entusiasmados a anunciar a localização do DevTools, que agora você pode usar em um dos dez idiomas além do inglês:</span><span class="sxs-lookup"><span data-stu-id="5494f-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5494f-121">Chinês \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="5494f-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5494f-122">Chinês \ (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="5494f-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="5494f-123">Francês – Fran-Fran&#231;ais</span><span class="sxs-lookup"><span data-stu-id="5494f-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5494f-124">Alemão – Deutsch</span><span class="sxs-lookup"><span data-stu-id="5494f-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="5494f-125">Italiano-Italiano</span><span class="sxs-lookup"><span data-stu-id="5494f-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5494f-126"> &#26085;&#26412;&#35486; japonês</span><span class="sxs-lookup"><span data-stu-id="5494f-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="5494f-127">Coreano- &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="5494f-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5494f-128">Português-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="5494f-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="5494f-129">Russo –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="5494f-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5494f-130">Espanhol-espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="5494f-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="5494f-131">O DevTools corresponde automaticamente ao idioma usado para o Microsoft Edge `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="5494f-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="5494f-132">Se quiser que o Microsoft Edge esteja em um idioma e seu DevTools permaneça em inglês, pressione `F1` na devtools para abrir [as configurações][Settings] e desabilitar o **idioma do navegador correspondente**.</span><span class="sxs-lookup"><span data-stu-id="5494f-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="5494f-134">O DevTools em alemão</span><span class="sxs-lookup"><span data-stu-id="5494f-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-135">As mensagens do **console** não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="5494f-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="5494f-136">Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma usado para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5494f-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="5494f-137">Se você quiser usar o DevTools em um idioma diferente daqueles que estão disponíveis, [tweet][PostTweetEdgeDevTools] conosco ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="5494f-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="5494f-138">Chromium problema [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="5494f-138">Chromium issue [#941561][CR941561]</span></span>  

### <span data-ttu-id="5494f-139">extensão do Microsoft Edge da WebDicas</span><span class="sxs-lookup"><span data-stu-id="5494f-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="5494f-140">A extensão WebDicas da Microsoft Edge permite que você examine facilmente sua página da Web e obtenha comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.</span><span class="sxs-lookup"><span data-stu-id="5494f-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="5494f-141">Leia mais em [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="5494f-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="5494f-143">A guia **dicas** no devtools quando a extensão do navegador da WebDicas está instalada</span><span class="sxs-lookup"><span data-stu-id="5494f-143">The **Hints** tab in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-144">[Experimente a extensão do navegador da webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="5494f-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="5494f-145">Depois de instalar a extensão, abra a DevTools e selecione a guia dicas.  Aqui, execute uma verificação de site personalizável.</span><span class="sxs-lookup"><span data-stu-id="5494f-145">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="5494f-146">Vá para [webhint.Io][WebhintBrowserExtension] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="5494f-146">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="5494f-147">Modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="5494f-147">3D View</span></span>  

<span data-ttu-id="5494f-148">Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do [modelo de objeto de documento \ (dom \)][MDNDocumentObjectModel] ou do contexto de empilhamento de [índice z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="5494f-148">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="O modo de exibição 3D no DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="5494f-150">O modo de exibição 3D no DevTools</span><span class="sxs-lookup"><span data-stu-id="5494f-150">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-151">Para acessar o modo de exibição 3D, pressione `Ctrl`  +  `Shift`  +  `P` , digite o **modo de exibição 3D** e selecione **Mostrar modo de exibição 3D**.</span><span class="sxs-lookup"><span data-stu-id="5494f-151">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="5494f-152">Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao modo de exibição 3D, portanto, envie-nos seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="5494f-152">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="5494f-153">Chromium problema [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="5494f-153">Chromium issue [#987787][CR987787]</span></span>  

### <span data-ttu-id="5494f-154">Extensões de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5494f-154">Visual Studio Code extensions</span></span>  

<span data-ttu-id="5494f-155">A equipe do DevTools também lançou algumas extensões para o [código do Visual Studio][VisualStudioCode] que permitem usar o poder do devtools diretamente do seu editor de texto!</span><span class="sxs-lookup"><span data-stu-id="5494f-155">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="5494f-156">Confira as extensões abaixo:</span><span class="sxs-lookup"><span data-stu-id="5494f-156">Check out the extensions below:</span></span>  

#### <span data-ttu-id="5494f-157">Elementos do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5494f-157">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="5494f-158">Use a ferramenta elementos de dentro do código do Visual Studio adicionando os [elementos para o Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] extensão de código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5494f-158">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="A ferramenta elementos no código do Visual Studio usando os elementos da extensão do Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="5494f-160">A ferramenta **elementos** no código do Visual Studio usando os elementos da extensão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5494f-160">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-161">Para obter mais informações, consulte os [elementos da extensão de código do Microsoft Edge Visual Studio][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="5494f-161">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="5494f-162">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5494f-162">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="5494f-163">Com o [depurador para extensão de código do Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio, depure o JavaScript executando no Microsoft Edge diretamente do código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5494f-163">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="O depurador para extensão do Microsoft Edge no código do Visual Studio" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="5494f-165">O depurador para extensão do Microsoft Edge no código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5494f-165">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-166">Para obter mais informações, confira [como depurar o Microsoft Edge pelo código do Visual Studio][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="5494f-166">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="5494f-167">Dica da web</span><span class="sxs-lookup"><span data-stu-id="5494f-167">webhint</span></span>  

<span data-ttu-id="5494f-168">A extensão de código do [webdica][VisualStudioMarketplaceWebhintExtension] Visual Studio usa `webhint` para melhorar sua página da Web enquanto você está escrevendo!</span><span class="sxs-lookup"><span data-stu-id="5494f-168">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="5494f-169">Esta extensão executa e relata os diagnósticos nos arquivos do espaço de trabalho com base na `webhint` análise.</span><span class="sxs-lookup"><span data-stu-id="5494f-169">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="A extensão de código do webdica Visual Studio analisando um arquivo. TSX no código do Visual Studio" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="5494f-171">A extensão de código do webdica Visual Studio analisando um `.tsx` arquivo no código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5494f-171">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-172">[Saiba mais sobre a extensão webdica de código do Visual Studio][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="5494f-172">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="5494f-173">Integração do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5494f-173">Visual Studio integration</span></span>  

<span data-ttu-id="5494f-174">No Visual Studio 2019 versão 16,2 ou posterior, use o depurador do Visual Studio para Depurar JavaScript em execução no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5494f-174">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="5494f-175">[Baixe o Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5494f-175">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="5494f-177">O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta</span><span class="sxs-lookup"><span data-stu-id="5494f-177">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-178">[Saiba mais sobre como depurar o Microsoft Edge do Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="5494f-178">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="5494f-179">Rastrear mensagens do console de prevenção</span><span class="sxs-lookup"><span data-stu-id="5494f-179">Tracking prevention Console messages</span></span>  

<span data-ttu-id="5494f-180">A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você contra acompanhamento de sites que ainda não visitou.</span><span class="sxs-lookup"><span data-stu-id="5494f-180">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="5494f-181">A configuração de prevenção de rastreamento padrão é o modo balanceado, que bloqueia os rastreadores de terceiros e os rastreadores mal-intencionados conhecidos para obter uma experiência que equilibre a compatibilidade com a privacidade e a compatibilidade com a Web.</span><span class="sxs-lookup"><span data-stu-id="5494f-181">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="5494f-182">Para fornecer a você mais informações sobre a compatibilidade de sua página da Web quando determinados rastreadores estão bloqueados, também adicionamos mensagens de aviso no console quando um controlador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5494f-182">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="5494f-184">Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador</span><span class="sxs-lookup"><span data-stu-id="5494f-184">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-185">[Leia mais sobre a prevenção de rastreamento e o equilíbrio entre a compatibilidade entre privacidade e Web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="5494f-185">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="5494f-186">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="5494f-186">Announcements from the Chromium project</span></span>  

<span data-ttu-id="5494f-187">As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 81 que contribuíram para o projeto de código-fonte aberto Chromium.</span><span class="sxs-lookup"><span data-stu-id="5494f-187">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="5494f-188">Suporte do moto G4 no modo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5494f-188">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="5494f-189">Depois de [habilitar a barra de ferramentas do dispositivo][DeviceToolbar], simule as dimensões de um visor moto G4 da lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="5494f-189">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulando um visor moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="5494f-191">Simulando um visor moto G4</span><span class="sxs-lookup"><span data-stu-id="5494f-191">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-192">Clique em [Mostrar quadro de dispositivo][DeviceFrame] para mostrar o hardware moto G4 em torno do visor.</span><span class="sxs-lookup"><span data-stu-id="5494f-192">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrando o hardware moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="5494f-194">Mostrando o hardware moto G4</span><span class="sxs-lookup"><span data-stu-id="5494f-194">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-195">Recursos relacionados:</span><span class="sxs-lookup"><span data-stu-id="5494f-195">Related features:</span></span>  

*   <span data-ttu-id="5494f-196">Abra o [menu de comando][CommandMenu] e execute o `Capture screenshot` comando para fazer uma captura de tela do visor que inclua o hardware moto G4 (após habilitar a **exibição do quadro de dispositivo**).</span><span class="sxs-lookup"><span data-stu-id="5494f-196">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="5494f-197">[Acelera a rede e a CPU][ThrottleNetworkAndCpu] para simular com mais precisão as condições de navegação de um usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="5494f-197">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="5494f-198">Chromium problema [#924693][CR924693]</span><span class="sxs-lookup"><span data-stu-id="5494f-198">Chromium issue [#924693][CR924693]</span></span>  

### <span data-ttu-id="5494f-199">Atualizações relacionadas a cookies</span><span class="sxs-lookup"><span data-stu-id="5494f-199">Cookie-related updates</span></span>  

#### <span data-ttu-id="5494f-200">Cookies bloqueados no painel cookies</span><span class="sxs-lookup"><span data-stu-id="5494f-200">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="5494f-201">O painel cookies no painel de aplicativos agora exibe cookies bloqueados com um plano de fundo amarelo.</span><span class="sxs-lookup"><span data-stu-id="5494f-201">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueados no painel cookies do painel do aplicativo" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="5494f-203">Cookies bloqueados no painel cookies do painel do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5494f-203">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-204">Chromium problema [#1030258][CR1030258]</span><span class="sxs-lookup"><span data-stu-id="5494f-204">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <span data-ttu-id="5494f-205">Prioridade do cookie no painel cookies</span><span class="sxs-lookup"><span data-stu-id="5494f-205">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="5494f-206">As tabelas de cookies nos painéis rede e aplicativo agora incluem uma coluna de **prioridade** .</span><span class="sxs-lookup"><span data-stu-id="5494f-206">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="5494f-207">Navegadores baseados em Chromium, como o Microsoft Edge, são os únicos navegadores que dão suporte à prioridade de cookies.</span><span class="sxs-lookup"><span data-stu-id="5494f-207">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="5494f-208">Chromium problema [#1026879][CR1026879]</span><span class="sxs-lookup"><span data-stu-id="5494f-208">Chromium issue [#1026879][CR1026879]</span></span>  

#### <span data-ttu-id="5494f-209">Editar todos os valores de cookies</span><span class="sxs-lookup"><span data-stu-id="5494f-209">Edit all cookie values</span></span>  

<span data-ttu-id="5494f-210">Todas as células nas tabelas de cookies são editáveis agora, exceto as células na coluna **tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5494f-210">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="5494f-211">Veja os [campos][CookiesFields] para obter uma explicação de cada coluna.</span><span class="sxs-lookup"><span data-stu-id="5494f-211">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Editando um valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="5494f-213">Editando um valor de cookie</span><span class="sxs-lookup"><span data-stu-id="5494f-213">Editing a cookie value</span></span>  
:::image-end:::  

#### <span data-ttu-id="5494f-214">Copiar como Node.js FETCH para incluir dados de cookies</span><span class="sxs-lookup"><span data-stu-id="5494f-214">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="5494f-215">Clique com o botão direito do mouse em uma solicitação de rede e selecione **copiar**  >  **cópia como Node.js FETCH** para obter uma `fetch` expressão que inclua dados de cookies.</span><span class="sxs-lookup"><span data-stu-id="5494f-215">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js Fetch" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="5494f-217">Copiar como Node.js Fetch</span><span class="sxs-lookup"><span data-stu-id="5494f-217">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-218">Chromium problema [#1029826][CR1029826]</span><span class="sxs-lookup"><span data-stu-id="5494f-218">Chromium issue [#1029826][CR1029826]</span></span>  

### <span data-ttu-id="5494f-219">Ícones mais precisos de manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5494f-219">More accurate web app manifest icons</span></span>  

<span data-ttu-id="5494f-220">Anteriormente, o painel de manifesto no painel do aplicativo enviou suas próprias solicitações para exibir os ícones de manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="5494f-220">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="5494f-221">O DevTools agora mostra o mesmo ícone de manifesto usado pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5494f-221">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Ícones no painel manifestar" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="5494f-223">Ícones no painel manifestar</span><span class="sxs-lookup"><span data-stu-id="5494f-223">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-224">Chromium problema [#985402][CR985402]</span><span class="sxs-lookup"><span data-stu-id="5494f-224">Chromium issue [#985402][CR985402]</span></span>  

### <span data-ttu-id="5494f-225">Passe o mouse sobre as propriedades do conteúdo CSS para ver os valores sem escape</span><span class="sxs-lookup"><span data-stu-id="5494f-225">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="5494f-226">Passe o mouse sobre o valor de uma `content` propriedade para ver a versão sem escape do valor.</span><span class="sxs-lookup"><span data-stu-id="5494f-226">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="5494f-227">Por exemplo, nesta [demonstração][CSSContentDemo] ao inspecionar o `p::after` pseudo elemento, você vê uma cadeia de caracteres de escape no painel estilos:</span><span class="sxs-lookup"><span data-stu-id="5494f-227">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="A cadeia de caracteres de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="5494f-229">A cadeia de caracteres de escape</span><span class="sxs-lookup"><span data-stu-id="5494f-229">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="5494f-230">Ao passar o mouse sobre o `content` valor, você vê o valor indesejado:</span><span class="sxs-lookup"><span data-stu-id="5494f-230">When you hover over the `content` value you see the unescaped value:</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="O valor não-escape" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="5494f-232">O valor não-escape</span><span class="sxs-lookup"><span data-stu-id="5494f-232">The unescaped value</span></span>  
:::image-end:::  

### <span data-ttu-id="5494f-233">Erros de mapa de origem mais detalhados no console</span><span class="sxs-lookup"><span data-stu-id="5494f-233">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="5494f-234">Agora, o console fornece mais detalhes sobre o motivo pelo qual um mapa de origem falhou ao carregar ou analisar.</span><span class="sxs-lookup"><span data-stu-id="5494f-234">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="5494f-235">Anteriormente, era fornecido um erro sem explicar o que aconteceu de errado.</span><span class="sxs-lookup"><span data-stu-id="5494f-235">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Um erro de carregamento do mapa de origem no console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="5494f-237">Um erro de carregamento do mapa de origem no console</span><span class="sxs-lookup"><span data-stu-id="5494f-237">A source map loading error in the Console</span></span>  
:::image-end:::  

### <span data-ttu-id="5494f-238">Configuração para desativar a rolagem após o final de um arquivo</span><span class="sxs-lookup"><span data-stu-id="5494f-238">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="5494f-239">Abra [configurações][Settings] e, em **Preferences**seguida, desabilite as  >  **fontes**  >  **de preferências permitem a rolagem do final do arquivo** para desativar o comportamento padrão da interface do usuário que permite rolar bem após o final de um arquivo no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="5494f-239">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Desativando permitir rolagem após o final do arquivo" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="5494f-241">Desativando **permitir rolagem após o fim do arquivo** em configurações</span><span class="sxs-lookup"><span data-stu-id="5494f-241">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="A rolagem após o final de um arquivo agora está desabilitada no painel fontes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="5494f-243">A rolagem após o final de um arquivo agora está desabilitada no painel fontes</span><span class="sxs-lookup"><span data-stu-id="5494f-243">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <span data-ttu-id="5494f-244">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5494f-244">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="5494f-245">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="5494f-245">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="5494f-246">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="5494f-246">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="5494f-247">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="5494f-247">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular um visor móvel-simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Documentos da Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Show Device frame-simula dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Documentos da Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Acelerar a rede e a CPU-simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Documentos da Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Documentos da Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Campos: Exibir, editar e Excluir cookies com o Microsoft Edge DevTools | Documentos da Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para extensão de código do Microsoft Edge Visual Studio"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos para extensão de código do Microsoft Edge Visual Studio"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Código do Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \ (Chromium \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem de blog do Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos do Microsoft Edge Insider"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixe o Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  

[CR924693]: https://crbug.com/924693 "Solicitação de recurso: Adicionar moto G4 à lista de modo de dispositivo | Erros de Chromium"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Erros de Chromium"  
[CR1026879]: https://crbug.com/1026879 "A guia cookies no console de desenvolvimento não mostra mais a prioridade | Erros de Chromium"  
[CR1029826]: https://crbug.com/1029826 "guia rede-> clique com o botão direito do mouse para solicitar-> copiar-> copiar como busca não copiar cookies | Erros de Chromium"  
[CR985402]: https://crbug.com/985402 "ícone de manifesto do aplicativo Web cadeias de caracteres de erro são confusas | Erros de Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com a WCAG | Erros de Chromium"  
[CR941561]: https://crbug.com/941561 "Possibilidade de localização do DevTools | Erros de Chromium"  
[CR987787]: https://crbug.com/987787 "Modo de exibição 3D dom | Erros de Chromium"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração de conteúdo CSS não escape"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  

[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Informações sobre acessibilidade"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (modelo de objeto de documento) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-índice | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensão do navegador webhint | documentação do webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio extensão de código | documentação do webhint"  

> [!NOTE]
> <span data-ttu-id="5494f-284">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="5494f-284">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5494f-285">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/01/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5494f-285">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5494f-287">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5494f-287">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  