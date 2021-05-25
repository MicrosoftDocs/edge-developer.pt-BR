---
description: Sublinhados ondulados realçam problemas de código na ferramenta Elements, linha do tempo de atualização do serviço de trabalho e muito mais.
title: Novidades no DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5f499a6c9f1109f80a9d459edf94ed2226734f19
ms.sourcegitcommit: 87ba918b0910373bb645615377709bf140dc9b19
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583456"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="601e5-104">Novidades no DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="601e5-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="601e5-105">Sublinhados ondulados realçam problemas de código e melhorias na ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="601e5-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="601e5-106">Na maioria das IDEs modernas, sublinhados ondulados em texto indicam erros de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="601e5-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="601e5-107">Na Microsoft Edge versão 91 ou posterior, sublinhados ondulados são exibidos em HTML no visor **DOM** da **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="601e5-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="601e5-108">Os sublinhados ondulados indicam problemas de código e sugestões relacionadas à acessibilidade, compatibilidade, desempenho e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="601e5-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="601e5-109">Para obter mais informações sobre como revisar e editar problemas, navegue até Encontrar e corrigir problemas com a ferramenta Microsoft Edge [DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="601e5-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="601e5-110">Para abrir a **ferramenta Problemas** e saber mais sobre o problema e como corrigi-lo, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="601e5-111">Selecione e segure `Shift` e escolha qualquer sublinhado ondulado.</span><span class="sxs-lookup"><span data-stu-id="601e5-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="601e5-112">Conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="601e5-113">Passe o mouse em qualquer sublinhado ondulado.</span><span class="sxs-lookup"><span data-stu-id="601e5-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="601e5-114">Abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="601e5-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="601e5-115">Escolha **Mostrar em Problemas**.</span><span class="sxs-lookup"><span data-stu-id="601e5-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Escolha o erro sublinhado na ferramenta Elements" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="601e5-117">Escolha o erro sublinhado na **ferramenta Elements**</span><span class="sxs-lookup"><span data-stu-id="601e5-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Exibir detalhes de erro na ferramenta Problemas" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="601e5-119">Exibir detalhes de erro na ferramenta **Problemas**</span><span class="sxs-lookup"><span data-stu-id="601e5-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="601e5-120">Saiba mais sobre o DevTools com dicas de ferramentas informativas</span><span class="sxs-lookup"><span data-stu-id="601e5-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="601e5-121">O recurso Dicas de Ferramentas do DevTools ajuda você a aprender sobre todas as diferentes ferramentas e painéis no DevTools.</span><span class="sxs-lookup"><span data-stu-id="601e5-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="601e5-122">Para desativar dicas de ferramenta, selecione `Esc` .</span><span class="sxs-lookup"><span data-stu-id="601e5-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="601e5-123">Para ativar dicas de ferramenta, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="601e5-124">Selecione `Ctrl` + `Shift` + `H` \(Windows/Linux\) ou `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="601e5-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="601e5-125">[Abra o Menu de Comando][DevtoolsCommandMenuIndexOpenCommandMenu] e digite `tooltips` .</span><span class="sxs-lookup"><span data-stu-id="601e5-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="601e5-126">Escolha **Personalizar e controlar o DevTools** \( \) > Ajuda Para alternar as dicas de ferramenta `...` \*\*\*\*  >  **DevTools**.</span><span class="sxs-lookup"><span data-stu-id="601e5-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="601e5-127">Além disso, se você ativar o experimento Modo de Foco e Dicas de Ferramentas [do DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] também poderá escolher o botão Alternar as Dicas de Ferramentas **de DevTools** \( \) na parte inferior da Barra de `?` **Atividades**.</span><span class="sxs-lookup"><span data-stu-id="601e5-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="601e5-128">Para exibir mais informações sobre como usar o DevTools, a turn on Tooltips e, em seguida, passe o mouse em cada região descrita do DevTools.</span><span class="sxs-lookup"><span data-stu-id="601e5-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Passe o mouse em qualquer lugar na região realçada da ferramenta Problemas para exibir mais detalhes" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="601e5-130">Passe o mouse em qualquer lugar na região realçada da **ferramenta Problemas** para exibir mais detalhes</span><span class="sxs-lookup"><span data-stu-id="601e5-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="601e5-131">Linha do tempo de atualização do trabalhador do serviço</span><span class="sxs-lookup"><span data-stu-id="601e5-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="601e5-132">Na Microsoft Edge versão 91 ou posterior, se você for um desenvolvedor do Progressive Web App ou do Service Worker, exibirá o ciclo de vida de atualização de seus Funcionários do Serviço como uma linha do tempo na ferramenta **Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="601e5-132">In Microsoft Edge version 91 or later, if you're a Progressive Web App or Service Worker developer, display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="601e5-133">Esse recurso ajuda você a entender o tempo gasto pelo Trabalhador do Serviço em cada uma das etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="601e5-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="601e5-134">Install</span><span class="sxs-lookup"><span data-stu-id="601e5-134">Install</span></span>**  
*   **<span data-ttu-id="601e5-135">Wait</span><span class="sxs-lookup"><span data-stu-id="601e5-135">Wait</span></span>**  
*   **<span data-ttu-id="601e5-136">Ativar</span><span class="sxs-lookup"><span data-stu-id="601e5-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Revise a Linha do Tempo no Ciclo de Atualizações do seu Trabalhador do Serviço" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="601e5-138">Revise a **Linha do** Tempo no Ciclo **de Atualizações** do seu Trabalhador do Serviço</span><span class="sxs-lookup"><span data-stu-id="601e5-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="601e5-139">Para obter mais informações sobre o ciclo de vida dos Funcionários do Serviço, navegue até [o ciclo de vida do Trabalhador do Serviço.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]</span><span class="sxs-lookup"><span data-stu-id="601e5-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="601e5-140">Para obter mais informações sobre ferramentas de depuração para Aplicativos Web Progressivos e Funcionários de Serviço no DevTools, navegue até [Service Worker improvements][DevtoolsServiceWorkerIndex].</span><span class="sxs-lookup"><span data-stu-id="601e5-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="601e5-141">Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até o Problema [1066604][CR1066604].</span><span class="sxs-lookup"><span data-stu-id="601e5-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="601e5-142">Os Aplicativos Web Progressivos não exibem mais avisos para ícones não quadrados</span><span class="sxs-lookup"><span data-stu-id="601e5-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="601e5-143">Na Microsoft Edge versão [90][DevtoolsWhatsNew202102Devtools] ou anterior, se o Manifesto do Aplicativo Web do seu PWA incluiu um ícone não quadrado, um aviso foi exibido na seção Erros e **Avisos** para cada ícone não quadrado.</span><span class="sxs-lookup"><span data-stu-id="601e5-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if the Web App Manifest of your PWA included a non-square icon, a warning was displayed in the **Errors and Warnings**  section for each non-square icon.</span></span>  <span data-ttu-id="601e5-144">Na Microsoft Edge versão 91 ou posterior, a seção **Manifesto** na ferramenta **Aplicativo** não exibirá avisos se você fornecer pelo menos um ícone quadrado.</span><span class="sxs-lookup"><span data-stu-id="601e5-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="601e5-145">Se você não fornecer ícones quadrados, um aviso exibirá a seguinte mensagem.</span><span class="sxs-lookup"><span data-stu-id="601e5-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="Na Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="601e5-147">Na Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado</span><span class="sxs-lookup"><span data-stu-id="601e5-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="Na Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="601e5-149">Na Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado</span><span class="sxs-lookup"><span data-stu-id="601e5-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="601e5-150">Para revisar erros e avisos em seu Manifesto do Aplicativo Web, navegue até a ferramenta **Aplicativo** e escolha a **seção Manifesto.**</span><span class="sxs-lookup"><span data-stu-id="601e5-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="601e5-151">Os erros e avisos estão listados no **título Erros e Avisos.**</span><span class="sxs-lookup"><span data-stu-id="601e5-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="601e5-152">Para obter mais informações sobre o Manifesto do Aplicativo Web, navegue até Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo [ao Sistema Operacional][ProgressiveWebAppsWebappmanifests].</span><span class="sxs-lookup"><span data-stu-id="601e5-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="601e5-153">Para criar ícones para incluir no Manifesto do Aplicativo Web, navegue até o Gerador de [Imagens do PWABuilder.][PwabuilderImagegenerator]</span><span class="sxs-lookup"><span data-stu-id="601e5-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="601e5-154">Para analisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [1185945][CR1185945].</span><span class="sxs-lookup"><span data-stu-id="601e5-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="601e5-155">O DevTools localizado agora tem suporte Chromium navegadores baseados em Chromium</span><span class="sxs-lookup"><span data-stu-id="601e5-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="601e5-156">A partir [Microsoft Edge versão 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools é exibido em seu próprio idioma.</span><span class="sxs-lookup"><span data-stu-id="601e5-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="601e5-157">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="601e5-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="601e5-158">A equipe Microsoft Edge DevTools, a equipe chrome DevTools e a equipe do Google Lighthouse colaboraram para fornecer a mesma experiência em todos os navegadores Chromium baseados em Chromium.</span><span class="sxs-lookup"><span data-stu-id="601e5-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="601e5-159">Para obter mais informações sobre como usar o DevTools em seu idioma, navegue até Alterar configurações de idioma [do DevTools.][DevtoolsCustomizeLocalization]</span><span class="sxs-lookup"><span data-stu-id="601e5-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="601e5-160">Para obter mais informações sobre a colaboração nesse recurso no Chromium de código aberto, navegue até [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="601e5-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge navegador e DevTools definido como japonês" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="601e5-162">Microsoft Edge navegador e DevTools definido como japonês</span><span class="sxs-lookup"><span data-stu-id="601e5-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="601e5-163">Usar o teclado para navegar até variáveis CSS</span><span class="sxs-lookup"><span data-stu-id="601e5-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="601e5-164">A partir [Microsoft Edge versão 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], o painel **Estilos** exibe variáveis CSS e fornece um link diretamente para a definição de cada variável.</span><span class="sxs-lookup"><span data-stu-id="601e5-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="601e5-165">Na Microsoft Edge versão 91 ou posterior, você pode usar as teclas de seta para navegar facilmente para variáveis CSS.</span><span class="sxs-lookup"><span data-stu-id="601e5-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="601e5-166">Para abrir a definição no painel **Estilos,** passe o mouse em uma variável e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="601e5-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="601e5-167">Para obter mais informações sobre variáveis CSS, navegue até [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span><span class="sxs-lookup"><span data-stu-id="601e5-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="601e5-168">Para analisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [1187735][CR1187735].</span><span class="sxs-lookup"><span data-stu-id="601e5-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="A variável CSS --theme-body-background realçada no painel Estilos" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="601e5-170">A `--theme-body-background` variável CSS realçada no painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="601e5-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="601e5-171">Os problemas são automaticamente resolvidos por gravidade</span><span class="sxs-lookup"><span data-stu-id="601e5-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="601e5-172">A **ferramenta Issues** exibe recomendações para melhorar seu site, incluindo acessibilidade, desempenho, segurança e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="601e5-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="601e5-173">Com base em seus comentários, os problemas agora são automaticamente resolvidos por gravidade.</span><span class="sxs-lookup"><span data-stu-id="601e5-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="601e5-174">Em cada categoria de comentários, cada problema marcado como **Erro** aparece primeiro, seguido de cada problema marcado como Aviso **,** em seguida, cada problema marcado como uma **Dica**.</span><span class="sxs-lookup"><span data-stu-id="601e5-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="601e5-175">Para ajudá-lo a refinar seus problemas, as opções de filtro extra são planejadas para uma atualização futura.</span><span class="sxs-lookup"><span data-stu-id="601e5-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="601e5-176">Para obter mais informações sobre como revisar problemas, navegue até Encontrar e corrigir problemas com a ferramenta Microsoft Edge [Problemas do DevTools.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="601e5-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="A ferramenta Issues exibe problemas organizados por gravidade" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="601e5-178">A **ferramenta Issues** exibe problemas organizados por gravidade</span><span class="sxs-lookup"><span data-stu-id="601e5-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="601e5-179">Microsoft Edge Ferramentas de desenvolvedor Visual Studio Code versão 1.1.7</span><span class="sxs-lookup"><span data-stu-id="601e5-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="601e5-180">O [Microsoft Edge Ferramentas para Visual Studio Code versão][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] 1.1.7 fornece o DevTools do Microsoft Edge versão [88][DevtoolsWhatsNew202011Devtools].</span><span class="sxs-lookup"><span data-stu-id="601e5-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="601e5-181">Essa extensão agora suporta ARM dispositivos e não depende mais do [Depurador para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extensão.</span><span class="sxs-lookup"><span data-stu-id="601e5-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="601e5-182">A versão 1.1.7 inclui as seguintes correções de bugs e melhorias.</span><span class="sxs-lookup"><span data-stu-id="601e5-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="601e5-183">Atualizou a confiabilidade do fechamento de destino.</span><span class="sxs-lookup"><span data-stu-id="601e5-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="601e5-184">Atualizou o painel lateral para atualizar automaticamente quando você depura destinos criados ou destruídos.</span><span class="sxs-lookup"><span data-stu-id="601e5-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="601e5-185">Adicionado um novo menu contextual que oferece acesso mais rápido às configurações de extensão e ao Changelog mais recente.</span><span class="sxs-lookup"><span data-stu-id="601e5-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="601e5-186">Atualizado e simplificado a versão da documentação de extensão, incluindo os recursos mais novos.</span><span class="sxs-lookup"><span data-stu-id="601e5-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="601e5-187">Para atualizar manualmente para a versão 1.1.7, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="601e5-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="601e5-188">Você pode registrar problemas e contribuir para a extensão no [repositório do GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="601e5-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="601e5-189">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="601e5-189">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a><span data-ttu-id="601e5-190">Visualizar o snap de rolagem CSS</span><span class="sxs-lookup"><span data-stu-id="601e5-190">Visualize CSS scroll-snap</span></span>  

<span data-ttu-id="601e5-191">Agora você pode alternar o `scroll-snap` selo na ferramenta **Elements** para inspecionar o alinhamento de rolagem CSS.</span><span class="sxs-lookup"><span data-stu-id="601e5-191">You may now toggle the `scroll-snap` badge in the **Elements** tool to inspect the CSS scroll-snap alignment.</span></span>  <span data-ttu-id="601e5-192">Quando um elemento HTML em sua página da Web é aplicado a ela, um selo é exibido ao lado dele `scroll-snap-type` `scroll-snap` na ferramenta **Elements.**</span><span class="sxs-lookup"><span data-stu-id="601e5-192">When an HTML element on your webpage has `scroll-snap-type` applied to it, a `scroll-snap` badge displays next to it in the **Elements** tool.</span></span>  <span data-ttu-id="601e5-193">Escolha o selo para ativar \(ou desativar\) a exibição de uma sobreposição de rolagem na página da Web.</span><span class="sxs-lookup"><span data-stu-id="601e5-193">Choose the badge to turn on \(or off\) the display of a scroll-snap overlay on the webpage.</span></span>  <span data-ttu-id="601e5-194">Para revisar uma página da Web de exemplo, navegue até [Scroll Ajustar Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span><span class="sxs-lookup"><span data-stu-id="601e5-194">To review an example webpage, navigate to [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span></span>  <span data-ttu-id="601e5-195">No exemplo, os pontos são exibidos em bordas de encaixe.</span><span class="sxs-lookup"><span data-stu-id="601e5-195">In the example, dots display on snap edges.</span></span>  <span data-ttu-id="601e5-196">A porta de rolagem tem um contorno sólido enquanto os itens de encaixe têm estruturas de contorno.</span><span class="sxs-lookup"><span data-stu-id="601e5-196">The scroll port has a solid outline while the snap items have dash outlines.</span></span>  <span data-ttu-id="601e5-197">O preenchimento de rolagem é preenchido em verde enquanto a margem de rolagem é preenchida em laranja.</span><span class="sxs-lookup"><span data-stu-id="601e5-197">The scroll padding is filled in green while the scroll margin is filled in orange.</span></span>  <span data-ttu-id="601e5-198">Para revisar o histórico desse recurso no Chromium de código aberto, navegue até o Problema [862450][CR862450].</span><span class="sxs-lookup"><span data-stu-id="601e5-198">To review the history of this feature in the Chromium open-source project, navigate to Issue [862450][CR862450].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS scroll-snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   <span data-ttu-id="601e5-200">CSS scroll-snap</span><span class="sxs-lookup"><span data-stu-id="601e5-200">CSS scroll-snap</span></span>  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a><span data-ttu-id="601e5-201">Nova ferramenta Inspetor de Memória</span><span class="sxs-lookup"><span data-stu-id="601e5-201">New Memory Inspector tool</span></span>  

<span data-ttu-id="601e5-202">Use a nova **ferramenta Inspetor de Memória** para inspecionar uma memória `ArrayBuffer` JavaScript e Wasm.</span><span class="sxs-lookup"><span data-stu-id="601e5-202">Use the new **Memory Inspector** tool to inspect an `ArrayBuffer` in JavaScript and Wasm memory.</span></span>  <span data-ttu-id="601e5-203">Abra a página da Web de demonstração Memória no [JS.][GlitchMemoryInspectorDemoJsHtml]</span><span class="sxs-lookup"><span data-stu-id="601e5-203">Open the [Memory in JS][GlitchMemoryInspectorDemoJsHtml] demo webpage.</span></span>  <span data-ttu-id="601e5-204">Na ferramenta **Fontes,** abra o `memory-write-wasm` arquivo e de definir um ponto de interrupção na linha `0x03c` .</span><span class="sxs-lookup"><span data-stu-id="601e5-204">In the **Sources** tool, open the `memory-write-wasm` file, and set a breakpoint at line `0x03c`.</span></span>  <span data-ttu-id="601e5-205">Atualize a página da Web.</span><span class="sxs-lookup"><span data-stu-id="601e5-205">Refresh the webpage.</span></span>  <span data-ttu-id="601e5-206">Expanda **a seção Escopo** no painel de depurador.</span><span class="sxs-lookup"><span data-stu-id="601e5-206">Expand the **Scope** section in the debugger pane.</span></span>  <span data-ttu-id="601e5-207">O novo ícone é exibido ao lado do **valor do buffer.**</span><span class="sxs-lookup"><span data-stu-id="601e5-207">The new icon is displayed next to the **buffer** value.</span></span>  <span data-ttu-id="601e5-208">Escolha-o para abrir a nova **ferramenta Inspetor de** Memória.</span><span class="sxs-lookup"><span data-stu-id="601e5-208">Choose it to open the new **Memory Inspector** tool.</span></span>  

<span data-ttu-id="601e5-209">Para saber mais sobre a depuração na ferramenta **Fontes,** navegue até Usando o [painel Depurador para depurar][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]código JavaScript .</span><span class="sxs-lookup"><span data-stu-id="601e5-209">To learn more about debugging in the **Sources** tool, navigate to [Using the Debugger pane to debug JavaScript code][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].</span></span>  <span data-ttu-id="601e5-210">Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1166577][CR1166577].</span><span class="sxs-lookup"><span data-stu-id="601e5-210">To review the history of this feature in the Chromium open-source project, navigate to Issue [1166577][CR1166577].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Ferramenta Inspetor de Memória" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   <span data-ttu-id="601e5-212">**Ferramenta inspetor de** memória</span><span class="sxs-lookup"><span data-stu-id="601e5-212">**Memory inspector** tool</span></span>  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a><span data-ttu-id="601e5-213">Novo painel de configurações do Selo na ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="601e5-213">New Badge settings pane in the Elements tool</span></span>  

<span data-ttu-id="601e5-214">Agora, use as **configurações de** Selo na ferramenta **Elementos** para ativar \(ou desativar\) selos individuais.</span><span class="sxs-lookup"><span data-stu-id="601e5-214">Now, use the **Badge settings** in the **Elements** tool to turn on \(or off\) individual badges.</span></span>  <span data-ttu-id="601e5-215">Use esse recurso para personalizar e manter o foco em selos importantes enquanto você inspeciona páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="601e5-215">Use this feature to customize and stay focused on important badges while you inspect webpages.</span></span>  <span data-ttu-id="601e5-216">Para exibir o painel de configurações de selo na parte superior da **ferramenta Elements,** conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-216">To display the badge settings pane at the top of the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="601e5-217">Passe o mouse em qualquer elemento.</span><span class="sxs-lookup"><span data-stu-id="601e5-217">Hover on any element.</span></span>  
1.  <span data-ttu-id="601e5-218">Abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="601e5-218">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="601e5-219">Escolha **Configurações de selo...**.</span><span class="sxs-lookup"><span data-stu-id="601e5-219">Choose **Badge settings...**.</span></span>  
    
<span data-ttu-id="601e5-220">Para exibir \(ou ocultar\) os selos, escolha \(ou remova\) a caixa de seleção ao lado do nome do selo.</span><span class="sxs-lookup"><span data-stu-id="601e5-220">To display \(or hide\) the badges, choose \(or remove\) the checkbox next to the badge name.</span></span>  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Painel de configurações de selo na ferramenta Elements" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   <span data-ttu-id="601e5-222">**Painel de configurações de** selo na **ferramenta Elements**</span><span class="sxs-lookup"><span data-stu-id="601e5-222">**Badge settings** pane in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a><span data-ttu-id="601e5-223">Visualização de imagem aprimorada com informações de proporção</span><span class="sxs-lookup"><span data-stu-id="601e5-223">Enhanced image preview with aspect ratio information</span></span>  

<span data-ttu-id="601e5-224">As visualizações de imagem no DevTools foram aprimoradas para exibir mais informações, incluindo os detalhes a seguir.</span><span class="sxs-lookup"><span data-stu-id="601e5-224">Image previews in the DevTools have been enhanced to display more information, including the following details.</span></span>  

*   <span data-ttu-id="601e5-225">Tamanho renderizado</span><span class="sxs-lookup"><span data-stu-id="601e5-225">Rendered size</span></span>  
*   <span data-ttu-id="601e5-226">Taxa de proporção renderizada</span><span class="sxs-lookup"><span data-stu-id="601e5-226">Rendered aspect ratio</span></span>  
*   <span data-ttu-id="601e5-227">Tamanho intrínseco</span><span class="sxs-lookup"><span data-stu-id="601e5-227">Intrinsic size</span></span>  
*   <span data-ttu-id="601e5-228">Taxa de proporção intrínseco</span><span class="sxs-lookup"><span data-stu-id="601e5-228">Intrinsic aspect ratio</span></span>  
*   <span data-ttu-id="601e5-229">Tamanho do arquivo</span><span class="sxs-lookup"><span data-stu-id="601e5-229">File size</span></span>  
    
<span data-ttu-id="601e5-230">As informações ajudam você a entender melhor suas imagens e aplicar a otimização.</span><span class="sxs-lookup"><span data-stu-id="601e5-230">The  information helps you better understand your images and apply optimization.</span></span>  <span data-ttu-id="601e5-231">As informações da taxa de proporção de imagem também estão disponíveis na **ferramenta Rede,** quando você escolhe uma visualização de imagem.</span><span class="sxs-lookup"><span data-stu-id="601e5-231">The image aspect ratio information is also available in the **Network** tool, when you choose an image preview.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="601e5-232">Na ferramenta **Elementos,** a visualização de imagem agora exibe mais informações sobre a imagem.</span><span class="sxs-lookup"><span data-stu-id="601e5-232">In the **Elements** tool, image preview now displays more information about the image.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="601e5-233">Além disso, as informações da taxa de proporção de imagem estão disponíveis na **ferramenta Rede,** quando você escolhe uma visualização de imagem.</span><span class="sxs-lookup"><span data-stu-id="601e5-233">Also, the image aspect ratio information is available in the **Network** tool, when you choose an image preview.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Visualização de imagem com informações de proporção na ferramenta Elemento" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         <span data-ttu-id="601e5-235">Visualização de imagem com informações de proporção na **ferramenta Elemento**</span><span class="sxs-lookup"><span data-stu-id="601e5-235">Image preview with aspect ratio information in the **Element** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Informações sobre a taxa de proporção de imagem na ferramenta Rede" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         <span data-ttu-id="601e5-237">Informações sobre a taxa de proporção de imagem na **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="601e5-237">Image aspect ratio information in the **Network** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="601e5-238">Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problemas [1149832][CR1149832] e [1170656][CR1170656].</span><span class="sxs-lookup"><span data-stu-id="601e5-238">To review the history of this feature in the Chromium open-source project, navigate to Issues [1149832][CR1149832] and [1170656][CR1170656].</span></span>  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a><span data-ttu-id="601e5-239">Novas opções para configurar codificações de conteúdo na ferramenta Condições de rede</span><span class="sxs-lookup"><span data-stu-id="601e5-239">New options to configure Content-Encodings in the Network conditions tool</span></span> 

<span data-ttu-id="601e5-240">Na ferramenta **Rede,** escolha o novo botão Mais condições de **rede...** ao lado do menu suspenso **Throttling** para abrir a **ferramenta Condições de** rede.</span><span class="sxs-lookup"><span data-stu-id="601e5-240">In the **Network** tool, choose the new **More network conditions...** button next to the **Throttling** dropdown menu to open the **Network conditions** tool.</span></span>  <span data-ttu-id="601e5-241">Para testar se as respostas do servidor estão codificadas corretamente para navegadores que não suportam [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]ou outro futuro, concluam `Content-Encoding` as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-241">To test if server responses are correctly encoded for browsers that don't support [gzip][GnuSoftwareGzipManual], [brotli][|::ref1::|Main], or another future `Content-Encoding`, complete the following actions.</span></span>  

1.  <span data-ttu-id="601e5-242">Abra a **ferramenta Condições de** rede</span><span class="sxs-lookup"><span data-stu-id="601e5-242">Open the **Network conditions** tool</span></span>
1.  <span data-ttu-id="601e5-243">Navegue **até Codificações de**Conteúdo Aceito.</span><span class="sxs-lookup"><span data-stu-id="601e5-243">Navigate to **Accepted Content-Encodings**.</span></span> 
1.  <span data-ttu-id="601e5-244">Remova a caixa de seleção ao lado `Content-Encoding` do que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="601e5-244">Remove the checkbox next to the `Content-Encoding` you want to test.</span></span>  
    
<span data-ttu-id="601e5-245">Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1162042][CR1162042].</span><span class="sxs-lookup"><span data-stu-id="601e5-245">To review the history of this feature in the Chromium open-source project, navigate to Issue [1162042][CR1162042].</span></span>  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Novas condições de rede mais... abre a ferramenta Condições de Rede para configurar a codificação de conteúdo" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   <span data-ttu-id="601e5-247">Novas **condições de rede... o botão** abre a ferramenta Condições **de** rede para configurar</span><span class="sxs-lookup"><span data-stu-id="601e5-247">New **More network conditions...** button opens the **Network conditions** tool to configure</span></span> `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a><span data-ttu-id="601e5-248">Aprimoramentos do painel de estilos</span><span class="sxs-lookup"><span data-stu-id="601e5-248">Styles pane enhancements</span></span>  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a><span data-ttu-id="601e5-249">Novo atalho para exibir o valor calculado no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="601e5-249">New shortcut to display computed value in the Styles pane</span></span>  

<span data-ttu-id="601e5-250">Agora, para exibir o valor CSS calculado no painel **Estilos,** conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-250">Now, to display the computed CSS value in the **Styles** pane, complete the following actions.</span></span>  

1.  <span data-ttu-id="601e5-251">Passe o mouse em uma propriedade CSS.</span><span class="sxs-lookup"><span data-stu-id="601e5-251">Hover on a CSS property.</span></span>  
1.  <span data-ttu-id="601e5-252">Abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="601e5-252">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="601e5-253">Escolha **Exibir valor calculado**.</span><span class="sxs-lookup"><span data-stu-id="601e5-253">Choose **View computed value**.</span></span>  
    
<span data-ttu-id="601e5-254">Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1076198][CR1076198].</span><span class="sxs-lookup"><span data-stu-id="601e5-254">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076198][CR1076198].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Novo atalho para exibir o valor calculado" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   <span data-ttu-id="601e5-256">Novo atalho para exibir o valor calculado</span><span class="sxs-lookup"><span data-stu-id="601e5-256">New shortcut to display computed value</span></span>  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a><span data-ttu-id="601e5-257">Suporte para a palavra-chave accent-color</span><span class="sxs-lookup"><span data-stu-id="601e5-257">Support for the accent-color keyword</span></span>  

<span data-ttu-id="601e5-258">A interface do usuário de preenchimento automático do painel **Estilos** agora detecta a palavra-chave CSS, que permite especificar a cor de destaque para controles de interface do usuário gerados `accent-color` pelo elemento.</span><span class="sxs-lookup"><span data-stu-id="601e5-258">The autocomplete UI of the **Styles** pane now detects the `accent-color` CSS keyword, which allows you to specify the accent color for UI controls generated by the element.</span></span>  <span data-ttu-id="601e5-259">Exemplos de controles de interface do usuário gerados por um elemento incluem caixas de seleção ou botões de rádio.</span><span class="sxs-lookup"><span data-stu-id="601e5-259">Examples of UI controls that are generated by an element include checkboxes or radio buttons.</span></span> <span data-ttu-id="601e5-260">Para obter mais informações sobre o status da implementação Chromium, navegue até Recurso: propriedade CSS de [cor de destaque.][ChromestatusFeature4752739957473280]</span><span class="sxs-lookup"><span data-stu-id="601e5-260">For more information about the status of the Chromium implementation, navigate to [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].</span></span>  <span data-ttu-id="601e5-261">Para ativar esse recurso, navegue até e de definir a caixa de `edge://flags#enable-experimental-web-platform-features` seleção como **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="601e5-261">To turn on this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and set the checkbox to **Enabled**.</span></span>  <span data-ttu-id="601e5-262">Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1092093][CR1092093].</span><span class="sxs-lookup"><span data-stu-id="601e5-262">To review the history of this feature in the Chromium open-source project, navigate to Issue [1092093][CR1092093].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="Palavra-chave CSS de cor de destaque" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` <span data-ttu-id="601e5-264">Palavra-chave CSS</span><span class="sxs-lookup"><span data-stu-id="601e5-264">CSS keyword</span></span>
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a><span data-ttu-id="601e5-265">Exibir detalhes sobre recursos bloqueados na exibição De detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="601e5-265">Display details about blocked features in the Frame details view</span></span>  

<span data-ttu-id="601e5-266">Política de Permissões é uma API de plataforma web que oferece a um site a capacidade de permitir ou bloquear o uso de recursos do navegador em um quadro individual ou em um que `iframe` ele incorpora.</span><span class="sxs-lookup"><span data-stu-id="601e5-266">Permissions Policy is a web platform API that gives a website the ability to allow or block the use of browser features in an individual frame or in an `iframe` that it embeds.</span></span> <span data-ttu-id="601e5-267">Para obter mais informações, navegue até [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span><span class="sxs-lookup"><span data-stu-id="601e5-267">For more information, navigate to [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span></span>  <span data-ttu-id="601e5-268">Para exibir os detalhes sobre por que um recurso é bloqueado, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-268">To display the details on why a feature is blocked, complete the following actions.</span></span>  

1.  <span data-ttu-id="601e5-269">Navegue até [Política de Permissões OOPIF.][GlitchPermissionPolicyDemoMain]</span><span class="sxs-lookup"><span data-stu-id="601e5-269">Navigate to [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].</span></span>  
1.  <span data-ttu-id="601e5-270">Navegue até **a ferramenta Application.**</span><span class="sxs-lookup"><span data-stu-id="601e5-270">Navigate to the **Application** tool.</span></span>  
1.  <span data-ttu-id="601e5-271">Escolha um quadro.</span><span class="sxs-lookup"><span data-stu-id="601e5-271">Choose a frame.</span></span>  
1.  <span data-ttu-id="601e5-272">Navegue até a **seção Política de Permissões.**</span><span class="sxs-lookup"><span data-stu-id="601e5-272">Navigate to the **Permissions Policy** section.</span></span>  
1.  <span data-ttu-id="601e5-273">Navegue até a **propriedade Disabled Features.**</span><span class="sxs-lookup"><span data-stu-id="601e5-273">Navigate to the **Disabled Features** property.</span></span>  
1.  <span data-ttu-id="601e5-274">Escolha **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="601e5-274">Choose **Show details**.</span></span>  
1.  <span data-ttu-id="601e5-275">Escolha o ícone ao lado de cada política para navegar até a solicitação de rede `iframe` ou que bloqueou o recurso.</span><span class="sxs-lookup"><span data-stu-id="601e5-275">Choose the icon next to each policy to navigate to the `iframe` or network request that blocked the feature.</span></span>  
    
<span data-ttu-id="601e5-276">Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="601e5-276">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Recursos bloqueados na exibição de detalhes do quadro" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   <span data-ttu-id="601e5-278">Recursos bloqueados na exibição de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="601e5-278">Blocked features in the Frame details view</span></span>  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a><span data-ttu-id="601e5-279">Filtrar experimentos na configuração Experimentos</span><span class="sxs-lookup"><span data-stu-id="601e5-279">Filter experiments in the Experiments setting</span></span>  

<span data-ttu-id="601e5-280">Encontre experimentos mais rápido com o novo filtro de experimento.</span><span class="sxs-lookup"><span data-stu-id="601e5-280">Find experiments quicker with the new experiment filter.</span></span>  <span data-ttu-id="601e5-281">Por exemplo, para ativar novos experimentos para problemas de código, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-281">For example, to turn on new experiments for code issues, complete the following actions.</span></span>
``

1.  <span data-ttu-id="601e5-282">Navegue **até Configurações**  >  **Experimentos**.</span><span class="sxs-lookup"><span data-stu-id="601e5-282">Navigate to **Settings** > **Experiments**.</span></span>  
1.  <span data-ttu-id="601e5-283">Navegue até a **caixa de texto** Filtro.</span><span class="sxs-lookup"><span data-stu-id="601e5-283">Navigate to the **Filter** textbox.</span></span>  
1.  <span data-ttu-id="601e5-284">Digite `issues`.</span><span class="sxs-lookup"><span data-stu-id="601e5-284">Type `issues`.</span></span>  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtrar experimentos na configuração Experimentos" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   <span data-ttu-id="601e5-286">Filtrar experimentos na **configuração Experimentos**</span><span class="sxs-lookup"><span data-stu-id="601e5-286">Filter experiments in the **Experiments** setting</span></span>  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a><span data-ttu-id="601e5-287">Nova coluna Vary Header no painel de armazenamento de cache</span><span class="sxs-lookup"><span data-stu-id="601e5-287">New Vary Header column in the Cache storage pane</span></span>  

<span data-ttu-id="601e5-288">Use a nova `Vary Header` coluna no painel Cache **Armazenamento** para exibir os valores de cabeçalho de resposta [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP.</span><span class="sxs-lookup"><span data-stu-id="601e5-288">Use the new `Vary Header` column in the **Cache Storage** pane to display the [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP response header values.</span></span>  <span data-ttu-id="601e5-289">Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1186049][CR1186049].</span><span class="sxs-lookup"><span data-stu-id="601e5-289">To review the history of this feature in the Chromium open-source project, navigate to Issue [1186049][CR1186049].</span></span>  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Coluna Vary Header" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   <span data-ttu-id="601e5-291">Coluna Vary Header</span><span class="sxs-lookup"><span data-stu-id="601e5-291">Vary Header column</span></span>  
:::image-end:::  

### <a name="sources-tool-improvements"></a><span data-ttu-id="601e5-292">Melhorias da ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="601e5-292">Sources tool improvements</span></span>  

#### <a name="support-for-new-javascript-features"></a><span data-ttu-id="601e5-293">Suporte para novos recursos JavaScript</span><span class="sxs-lookup"><span data-stu-id="601e5-293">Support for new JavaScript features</span></span>  

<span data-ttu-id="601e5-294">Agora, o DevTools suporta a nova marca privada verifica [a.k.a. #foo no][V8DevFeaturesPrivateBrandChecks] recurso de idioma JavaScript obj.</span><span class="sxs-lookup"><span data-stu-id="601e5-294">DevTools now support the new [Private brand checks a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript language feature.</span></span>  <span data-ttu-id="601e5-295">O recurso de verificações de marca privada estende o [operador in][MdnDocsWebJavascriptReferenceOperatorsIn] para dar suporte a campos de [classe privada][V8DevFeaturesClassFieldsPrivateClassFields] em um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="601e5-295">The private brand checks feature extends the [in operator][MdnDocsWebJavascriptReferenceOperatorsIn] to support [Private class fields][V8DevFeaturesClassFieldsPrivateClassFields] on a specific object.</span></span>  <span data-ttu-id="601e5-296">Experimente nas ferramentas **Console** e **Sources.**</span><span class="sxs-lookup"><span data-stu-id="601e5-296">Try it in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="601e5-297">Além disso, para inspecionar os campos privados, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="601e5-297">Also, to inspect the private fields, complete the following actions.</span></span>  

1.  <span data-ttu-id="601e5-298">Navegue até o painel **de depurador.**</span><span class="sxs-lookup"><span data-stu-id="601e5-298">Navigate to **debugger** pane.</span></span>  
1.  <span data-ttu-id="601e5-299">Navegue até a **seção Escopo.**</span><span class="sxs-lookup"><span data-stu-id="601e5-299">Navigate to the **Scope** section.</span></span>  
    
<span data-ttu-id="601e5-300">Para revisar o histórico desse recurso no Chromium de código aberto, navegue até o Problema [11374][CR11374].</span><span class="sxs-lookup"><span data-stu-id="601e5-300">To review the history of this feature in the Chromium open-source project, navigate to Issue [11374][CR11374].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="Verificações de marca privada do JavaScript" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   <span data-ttu-id="601e5-302">Verificações de marca privada do JavaScript</span><span class="sxs-lookup"><span data-stu-id="601e5-302">JavaScript private brand checks</span></span>  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a><span data-ttu-id="601e5-303">Suporte aprimorado para depuração de pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="601e5-303">Enhanced support for breakpoints debugging</span></span>  

<span data-ttu-id="601e5-304">Os pacotes JavaScript modernos, como [Webpack][WebpackJsMain]e [Rollup,][RollupjsMain] suportam a divisão de código.</span><span class="sxs-lookup"><span data-stu-id="601e5-304">Modern JavaScript bundlers like [Webpack][WebpackJsMain], and [Rollup][RollupjsMain] support code splitting.</span></span>  <span data-ttu-id="601e5-305">Para saber mais sobre a divisão de código, navegue até [Divisão de código][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span><span class="sxs-lookup"><span data-stu-id="601e5-305">To learn more about code splitting, navigate to [Code splitting][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span></span>  <span data-ttu-id="601e5-306">Na Microsoft Edge versão 90 ou anterior, o DevTools apenas definirá pontos de interrupção em um único pacote.</span><span class="sxs-lookup"><span data-stu-id="601e5-306">In Microsoft Edge version 90 or earlier, DevTools only set breakpoints in a single bundle.</span></span>  <span data-ttu-id="601e5-307">Na Microsoft Edge versão 91 ou posterior, o DevTools define corretamente pontos de interrupção em vários pacotes quando você depura um componente compartilhado.</span><span class="sxs-lookup"><span data-stu-id="601e5-307">In Microsoft Edge version 91 or later, DevTools properly sets breakpoints in multiple bundles when you debug a shared component.</span></span>  <span data-ttu-id="601e5-308">Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problemas [1142705][CR1142705], [979000][CR979000]e [1180794][CR1180794].</span><span class="sxs-lookup"><span data-stu-id="601e5-308">To review the history of this feature in the Chromium open-source project, navigate to Issues [1142705][CR1142705], [979000][CR979000], and [1180794][CR1180794].</span></span>  

#### <a name="support-hover-preview-with-bracket-notation"></a><span data-ttu-id="601e5-309">Suporte à visualização de foco com notação de colchete</span><span class="sxs-lookup"><span data-stu-id="601e5-309">Support hover preview with bracket notation</span></span>  

<span data-ttu-id="601e5-310">O DevTools agora suporta a visualização de foco em expressões de membro JavaScript que usam `[]` a notação na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="601e5-310">DevTools now support hover preview on JavaScript member expressions that use the `[]` notation in the **Sources** tool.</span></span>  <span data-ttu-id="601e5-311">Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1178305][CR1178305].</span><span class="sxs-lookup"><span data-stu-id="601e5-311">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178305][CR1178305].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Suporte à visualização de foco com notação []" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   <span data-ttu-id="601e5-313">Suporte à visualização de foco `[]` com notação</span><span class="sxs-lookup"><span data-stu-id="601e5-313">Support hover preview with `[]` notation</span></span>  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a><span data-ttu-id="601e5-314">Contorno aprimorado de arquivos HTML</span><span class="sxs-lookup"><span data-stu-id="601e5-314">Improved outline of HTML files</span></span>  

<span data-ttu-id="601e5-315">O DevTools agora tem melhor suporte de contorno para `.html` arquivos.</span><span class="sxs-lookup"><span data-stu-id="601e5-315">DevTools now has better outline support for `.html` files.</span></span>  <span data-ttu-id="601e5-316">Na ferramenta **Fontes,** abra o `.html` arquivo.</span><span class="sxs-lookup"><span data-stu-id="601e5-316">In the **Sources** tool, open the `.html` file.</span></span>  <span data-ttu-id="601e5-317">Para ativar \(ou desativar\) o contorno de código, selecione em `Ctrl` + `Shift` + `O` Windows/Linux `Cmd` + `Shift` + `O` ou no macOS.</span><span class="sxs-lookup"><span data-stu-id="601e5-317">To turn on \(or off\) the code outline, select `Ctrl`+`Shift`+`O` on Windows/Linux or `Cmd`+`Shift`+`O` on macOS.</span></span>  <span data-ttu-id="601e5-318">Na figura a seguir, o DevTools lista corretamente todas as funções no contorno.</span><span class="sxs-lookup"><span data-stu-id="601e5-318">In the following figure, DevTools now correctly list all functions in the outline.</span></span>  <span data-ttu-id="601e5-319">Anteriormente, o DevTools exibia apenas algumas das funções.</span><span class="sxs-lookup"><span data-stu-id="601e5-319">Previously, DevTools only displayed some of the functions.</span></span>  <span data-ttu-id="601e5-320">Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problemas [761019][CR761019] e [1191465][CR1191465].</span><span class="sxs-lookup"><span data-stu-id="601e5-320">To review the history of this feature in the Chromium open-source project, navigate to Issues [761019][CR761019] and [1191465][CR1191465].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Contorno aprimorado de arquivos HTML" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   <span data-ttu-id="601e5-322">Contorno aprimorado de arquivos HTML</span><span class="sxs-lookup"><span data-stu-id="601e5-322">Improved outline of HTML files</span></span>  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a><span data-ttu-id="601e5-323">Rastreamentos de pilha de erros apropriados para depuração de Wasm</span><span class="sxs-lookup"><span data-stu-id="601e5-323">Proper error stack traces for Wasm debugging</span></span>  

<span data-ttu-id="601e5-324">Na Microsoft Edge versão 90 ou anterior, o DevTools exibia apenas referências genéricas de Wasm em Rastreamentos de pilha de erro.</span><span class="sxs-lookup"><span data-stu-id="601e5-324">In Microsoft Edge version 90 or earlier, DevTools only displayed generic Wasm references in Error stack traces.</span></span>  <span data-ttu-id="601e5-325">Na Microsoft Edge versão 91 ou posterior, o DevTools resolve solicitações de função em linha e exibe o local de origem em Rastreamentos de pilha de erro para depuração de Wasm.</span><span class="sxs-lookup"><span data-stu-id="601e5-325">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays the source location in Error stack traces for Wasm debugging.</span></span>  <span data-ttu-id="601e5-326">Para saber mais sobre Rastreamentos de pilha de erro no **Console,** navegue até [o erro][DevtoolsConsoleApiError].</span><span class="sxs-lookup"><span data-stu-id="601e5-326">To learn more about Error stack traces in the **Console**, navigate to [error][DevtoolsConsoleApiError].</span></span>  

<span data-ttu-id="601e5-327">Na Microsoft Edge versão 91 ou posterior, o DevTools resolve solicitações de função em linha e exibe rastreamentos de pilha de erros apropriados para depuração de Wasm.</span><span class="sxs-lookup"><span data-stu-id="601e5-327">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays proper error stack traces for Wasm debugging.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="601e5-328">Na Microsoft Edge versão 90 e anterior, o local de origem não é exibido nos rastreamentos de pilha error.</span><span class="sxs-lookup"><span data-stu-id="601e5-328">In Microsoft Edge version 90 and earlier, the source location doesn't display in the Error stack traces.</span></span>  <span data-ttu-id="601e5-329">Os locais de origem incluem `dsquare` .</span><span class="sxs-lookup"><span data-stu-id="601e5-329">Source locations include `dsquare`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="601e5-330">Na Microsoft Edge versão 91 e posterior, o local de origem é exibido nos rastreamentos de pilha error.</span><span class="sxs-lookup"><span data-stu-id="601e5-330">In Microsoft Edge version 91 and later, the source location displays in the Error stack traces.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Rastreamentos de pilha de erros anteriores para depuração de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         <span data-ttu-id="601e5-332">Rastreamentos de pilha de erros apropriados para depuração de Wasm</span><span class="sxs-lookup"><span data-stu-id="601e5-332">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Rastreamentos de pilha de erros apropriados para depuração de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         <span data-ttu-id="601e5-334">Rastreamentos de pilha de erros apropriados para depuração de Wasm</span><span class="sxs-lookup"><span data-stu-id="601e5-334">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="601e5-335">Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1189161][CR1189161].</span><span class="sxs-lookup"><span data-stu-id="601e5-335">To review the history of this feature in the Chromium open-source project, navigate to Issue [1189161][CR1189161].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="601e5-336">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="601e5-336">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="601e5-337">Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="601e5-337">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="601e5-338">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="601e5-338">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="601e5-339">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="601e5-339">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Usando o DevTools em outros idiomas - Novidades no DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Novidades no DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "Definições de variável CSS no painel Estilos - Novidades no DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Novidades no DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Ferramentas de grupo juntas no Modo de Foco - Novidades no DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Abra o Menu de Comando - Execute comandos com o menu Microsoft Edge DevTools Command | Microsoft Docs"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error - Console API reference | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Alterar configurações de idioma do DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Melhorias do Service Worker | Microsoft Docs"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Usando o painel Depurador para depurar código JavaScript - Visão geral da ferramenta sources | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "O ciclo de vida do Trabalhador do Serviço - Use Os Trabalhadores do Serviço para gerenciar solicitações de rede e notificações por push | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Use o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao sistema operacional | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace de Extensões | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador do Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Recurso: propriedade CSS de cor de destaque | Status da plataforma Chrome"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Cores de destaque do widget: a propriedade accent-color - CSS Basic User Interface Module Level 4 | Rascunhos do Editor do Grupo de Trabalho CSS"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR11374]: https://crbug.com/v8/11374 "Problema 11374: Implementar a verificação de marca ergonómica para campos privados"  
[CR761019]: https://crbug.com/761019 "Problema 761019: &quot;Ir para o símbolo&quot; perde a primeira função e prefere uma combinação pior se contiver todos os caracteres digitados"  
[CR862450]: https://crbug.com/862450 "Problema 862450: [css-scroll-snap] Considere adicionar o recurso Devtools para o snap de rolagem css"  
[CR979000]: https://crbug.com/979000 "Problema 979000: Mapas de origem com caminhos de fontes de colisão não funcionam."  
[CR1066604]: https://crbug.com/1066604 "Problema 1066604: DevTools: consulte detalhes sobre a instalação do ServiceWorker e ativação de eventos | Chromium bugs"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 "Problema 1076198: [Solicitação de Recurso] Pule para a propriedade computada da `styles` guia"  
[CR1092093]: "Problema 1092093: Tornar os controles de formulário mais estilizáveis de cor, dando suporte à https://crbug.com/1092093 propriedade CSS 'accent-color'"  
[CR1136655]: https://crbug.com/1136655 "Problema 1136655: Devtools: Localização V2 | Chromium bugs"  
[CR1142705]: "Problema 1142705: os pontos de interrupção param de funcionar quando 2 sourcemaps apontam para o mesmo arquivo virtual ao usar https://crbug.com/1142705 o webpack"  
[CR1149832]: "Problema 1149832: Solicitação de recurso: visualização de imagem também deve https://crbug.com/1149832 mostrar o tamanho do arquivo"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Política de Permissões] Implementar o suporte do devtool para a política de permissões"  
[CR1162042]: https://crbug.com/1162042 "Problema 1162042: DevTools: suporte à desabilitação de gzip/brotli/jxl content-encoding"  
[CR1166577]: https://crbug.com/1166577 "Problema 1166577: ☂️ Inspetor de Memória Linear 1.0"  
[CR1170656]: https://crbug.com/1170656 "Problema 1170656: Mostrar proporção intrínseca"  
[CR1178305]: https://crbug.com/1178305 "Problema 1178305: o depurador não mostra o valor da propriedade de um elemento indexado quando ele está em foco"  
[CR1180794]: "Problema 1180794: Pontos de interrupção não funcionam com otimização de inlining do Compilador de https://crbug.com/1180794 Fechamento"  
[CR1185945]: "Problema 1185945: Aviso de manifesto implica que todos os ícones devem ser https://crbug.com/1185945 quadrados | Chromium bugs"  
[CR1186049]: https://crbug.com/1186049 "Problema 1186049: Coluna para Variar: header no cache Armazenamento visualizador"  
[CR1187735]: https://crbug.com/1187735 "Problema 1187735: Acessibilidade: MAS2.1.1: Teclado: não é possível invocar a função 'Var(..)' usando o | Chromium bugs"  
[CR1189161]: https://crbug.com/1189161 "Problema 1189161: `new Error` stacktraces não são transformados via ANÃO"  
[CR1191465]: https://crbug.com/1191465 "Problema 1191465: Ctrl+Shift+O quebrado em HTML"  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicação da Política de Permissões | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Memória no JS | Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Memória em Wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Scroll Ajustar Demo | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "Política de Permissões OOPIF | Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip: o programa de compactação de dados | Sistema Operacional GNU"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary - Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content | Grupo de trabalho HTTP do IETF"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Há três abordagens gerais para a divisão de código disponível: Pontos de Entrada: Código dividido manualmente usando a configuração de entrada.  Impedir duplicação: use dependências de entrada ou SplitChunksPlugin para deduzir e dividir partes.  Importações dinâmicas: divida o código por meio de chamadas de função em linha em módulos. - Divisão de código | webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propriedades personalizadas CSS (variáveis) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "no operador | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Gerador de Imagens | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "Marca privada verifica a.k.a. #foo no obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Campos de classe privada - Campos de classe pública e privada | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> <span data-ttu-id="601e5-398">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="601e5-398">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="601e5-399">A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-91) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="601e5-399">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="601e5-401">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="601e5-401">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
