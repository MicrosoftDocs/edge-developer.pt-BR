---
description: Sublinhados ondulados realçam problemas de código na ferramenta Elements, linha do tempo de atualização do serviço de trabalho e muito mais.
title: Novidades no DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3a2be4d309432de4421af73ca7b4d21734ad5221
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514423"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="65ee3-104">Novidades no DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="65ee3-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="65ee3-105">Sublinhados ondulados realçam problemas de código e melhorias na ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="65ee3-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="65ee3-106">Na maioria das IDEs modernas, sublinhados ondulados em texto indicam erros de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="65ee3-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="65ee3-107">No Microsoft Edge versão 91 ou posterior, sublinhados ondulados são exibidos em HTML na exibição **DOM** da **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="65ee3-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="65ee3-108">Os sublinhados ondulados indicam problemas de código e sugestões relacionadas à acessibilidade, compatibilidade, desempenho e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="65ee3-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="65ee3-109">Para obter mais informações sobre como revisar e editar problemas, navegue até Encontrar e corrigir problemas com a ferramenta Problemas do [Microsoft Edge DevTools][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="65ee3-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="65ee3-110">Para abrir a **ferramenta Problemas** e saber mais sobre o problema e como corrigi-lo, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="65ee3-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="65ee3-111">Selecione e segure `Shift` e escolha qualquer sublinhado ondulado.</span><span class="sxs-lookup"><span data-stu-id="65ee3-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="65ee3-112">Conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="65ee3-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="65ee3-113">Passe o mouse em qualquer sublinhado ondulado.</span><span class="sxs-lookup"><span data-stu-id="65ee3-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="65ee3-114">Abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="65ee3-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="65ee3-115">Escolha **Mostrar em Problemas**.</span><span class="sxs-lookup"><span data-stu-id="65ee3-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Escolha o erro sublinhado na ferramenta Elements" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="65ee3-117">Escolha o erro sublinhado na **ferramenta Elements**</span><span class="sxs-lookup"><span data-stu-id="65ee3-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Exibir detalhes de erro na ferramenta Problemas" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="65ee3-119">Exibir detalhes de erro na ferramenta **Problemas**</span><span class="sxs-lookup"><span data-stu-id="65ee3-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="65ee3-120">Saiba mais sobre o DevTools com dicas de ferramentas informativas</span><span class="sxs-lookup"><span data-stu-id="65ee3-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="65ee3-121">O recurso Dicas de Ferramentas do DevTools ajuda você a aprender sobre todas as diferentes ferramentas e painéis no DevTools.</span><span class="sxs-lookup"><span data-stu-id="65ee3-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="65ee3-122">Para desativar dicas de ferramenta, selecione `Esc` .</span><span class="sxs-lookup"><span data-stu-id="65ee3-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="65ee3-123">Para ativar dicas de ferramenta, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="65ee3-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="65ee3-124">Selecione `Ctrl` + `Shift` + `H` \(Windows/Linux\) ou `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="65ee3-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="65ee3-125">[Abra o Menu de Comando][DevtoolsCommandMenuIndexOpenCommandMenu] e digite `tooltips` .</span><span class="sxs-lookup"><span data-stu-id="65ee3-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="65ee3-126">Escolha **Personalizar e controlar o DevTools** \( \) > Ajuda Para alternar as dicas de ferramenta `...` \*\*\*\*  >  **DevTools**.</span><span class="sxs-lookup"><span data-stu-id="65ee3-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="65ee3-127">Além disso, se você ativar o experimento Modo de Foco e Dicas de Ferramentas [do DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] também poderá escolher o botão Alternar as Dicas de Ferramentas **de DevTools** \( \) na parte inferior da Barra de `?` **Atividades**.</span><span class="sxs-lookup"><span data-stu-id="65ee3-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="65ee3-128">Para exibir mais informações sobre como usar o DevTools, a turn on Tooltips e, em seguida, passe o mouse em cada região descrita do DevTools.</span><span class="sxs-lookup"><span data-stu-id="65ee3-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Passe o mouse em qualquer lugar na região realçada da ferramenta Problemas para exibir mais detalhes" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="65ee3-130">Passe o mouse em qualquer lugar na região realçada da **ferramenta Problemas** para exibir mais detalhes</span><span class="sxs-lookup"><span data-stu-id="65ee3-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="65ee3-131">Linha do tempo de atualização do trabalhador do serviço</span><span class="sxs-lookup"><span data-stu-id="65ee3-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="65ee3-132">No Microsoft Edge versão 91 ou posterior, se você for um desenvolvedor do Progressive Web App ou Service Worker, poderá exibir o ciclo de vida de atualização de seus Funcionários do Serviço como uma linha do tempo na ferramenta **Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="65ee3-132">In Microsoft Edge version 91 or later, if you are a Progressive Web App or Service Worker developer, you may display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="65ee3-133">Esse recurso ajuda você a entender o tempo gasto pelo Trabalhador do Serviço em cada uma das etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="65ee3-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="65ee3-134">Install</span><span class="sxs-lookup"><span data-stu-id="65ee3-134">Install</span></span>**  
*   **<span data-ttu-id="65ee3-135">Wait</span><span class="sxs-lookup"><span data-stu-id="65ee3-135">Wait</span></span>**  
*   **<span data-ttu-id="65ee3-136">Ativar</span><span class="sxs-lookup"><span data-stu-id="65ee3-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Revise a Linha do Tempo no Ciclo de Atualizações do seu Trabalhador do Serviço" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="65ee3-138">Revise a **Linha do** Tempo no Ciclo **de Atualizações** do seu Trabalhador do Serviço</span><span class="sxs-lookup"><span data-stu-id="65ee3-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="65ee3-139">Para obter mais informações sobre o ciclo de vida dos Funcionários do Serviço, navegue até [o ciclo de vida do Trabalhador do Serviço.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]</span><span class="sxs-lookup"><span data-stu-id="65ee3-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="65ee3-140">Para obter mais informações sobre ferramentas de depuração para Aplicativos Web Progressivos e Funcionários de Serviço no DevTools, navegue até [Service Worker improvements][DevtoolsServiceWorkerIndex].</span><span class="sxs-lookup"><span data-stu-id="65ee3-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="65ee3-141">Para revisar atualizações em tempo real sobre esse recurso no projeto de código aberto do Chromium, navegue até o Problema [1066604][CR1066604].</span><span class="sxs-lookup"><span data-stu-id="65ee3-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="65ee3-142">Os Aplicativos Web Progressivos não exibem mais avisos para ícones não quadrados</span><span class="sxs-lookup"><span data-stu-id="65ee3-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="65ee3-143">No Microsoft Edge versão [90][DevtoolsWhatsNew202102Devtools] ou anterior, se você incluiu um ícone não quadrado no Manifesto do Aplicativo Web do seu PWA, a seção **Manifesto** na ferramenta **Aplicativo** exibiu um aviso em Erros e **Avisos** para cada ícone não quadrado.</span><span class="sxs-lookup"><span data-stu-id="65ee3-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if you included a non-square icon in the Web App Manifest of your PWA, the **Manifest** section in the **Application** tool displayed a warning under **Errors and Warnings** for each non-square icon.</span></span>  <span data-ttu-id="65ee3-144">No Microsoft Edge versão 91 ou posterior, a seção **Manifesto** na ferramenta **Aplicativo** não exibirá avisos se você fornecer pelo menos um ícone quadrado.</span><span class="sxs-lookup"><span data-stu-id="65ee3-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="65ee3-145">Se você não fornecer ícones quadrados, um aviso exibirá a seguinte mensagem.</span><span class="sxs-lookup"><span data-stu-id="65ee3-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="No Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="65ee3-147">No Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado</span><span class="sxs-lookup"><span data-stu-id="65ee3-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="No Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="65ee3-149">No Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado</span><span class="sxs-lookup"><span data-stu-id="65ee3-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="65ee3-150">Para revisar erros e avisos em seu Manifesto do Aplicativo Web, navegue até a ferramenta **Aplicativo** e escolha a **seção Manifesto.**</span><span class="sxs-lookup"><span data-stu-id="65ee3-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="65ee3-151">Os erros e avisos estão listados no **título Erros e Avisos.**</span><span class="sxs-lookup"><span data-stu-id="65ee3-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="65ee3-152">Para obter mais informações sobre o Manifesto do Aplicativo Web, navegue até Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo [ao Sistema Operacional][ProgressiveWebAppsWebappmanifests].</span><span class="sxs-lookup"><span data-stu-id="65ee3-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="65ee3-153">Para criar ícones para incluir no Manifesto do Aplicativo Web, navegue até o Gerador de [Imagens do PWABuilder.][PwabuilderImagegenerator]</span><span class="sxs-lookup"><span data-stu-id="65ee3-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="65ee3-154">Para revisar atualizações em tempo real sobre esse recurso no projeto de código aberto do Chromium, navegue até o Problema [1185945][CR1185945].</span><span class="sxs-lookup"><span data-stu-id="65ee3-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="65ee3-155">DevTools localizado agora tem suporte em navegadores baseados em Chromium</span><span class="sxs-lookup"><span data-stu-id="65ee3-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="65ee3-156">A partir [do Microsoft Edge versão 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], o Microsoft Edge DevTools é exibido em seu próprio idioma.</span><span class="sxs-lookup"><span data-stu-id="65ee3-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="65ee3-157">Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code em seu idioma nativo, não apenas em inglês.</span><span class="sxs-lookup"><span data-stu-id="65ee3-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="65ee3-158">A equipe do Microsoft Edge DevTools, a equipe do Chrome DevTools e a equipe do Google Lighthouse colaboraram para fornecer a mesma experiência em todos os navegadores baseados em Chromium.</span><span class="sxs-lookup"><span data-stu-id="65ee3-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="65ee3-159">Para obter mais informações sobre como usar o DevTools em seu idioma, navegue até Alterar configurações de idioma [do DevTools.][DevtoolsCustomizeLocalization]</span><span class="sxs-lookup"><span data-stu-id="65ee3-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="65ee3-160">Para obter mais informações sobre a colaboração neste recurso no projeto de código aberto do Chromium, navegue até [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="65ee3-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Navegador do Microsoft Edge e DevTools definido como japonês" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="65ee3-162">Navegador do Microsoft Edge e DevTools definido como japonês</span><span class="sxs-lookup"><span data-stu-id="65ee3-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="65ee3-163">Usar o teclado para navegar até variáveis CSS</span><span class="sxs-lookup"><span data-stu-id="65ee3-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="65ee3-164">A partir [do Microsoft Edge versão 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], o painel **Estilos** exibe variáveis CSS e fornece um link diretamente para a definição de cada variável.</span><span class="sxs-lookup"><span data-stu-id="65ee3-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="65ee3-165">No Microsoft Edge versão 91 ou posterior, você pode usar as teclas de seta para navegar facilmente para variáveis CSS.</span><span class="sxs-lookup"><span data-stu-id="65ee3-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="65ee3-166">Para abrir a definição no painel **Estilos,** passe o mouse em uma variável e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="65ee3-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="65ee3-167">Para obter mais informações sobre variáveis CSS, navegue até [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span><span class="sxs-lookup"><span data-stu-id="65ee3-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="65ee3-168">Para revisar atualizações em tempo real sobre esse recurso no projeto de código aberto do Chromium, navegue até o Problema [1187735][CR1187735].</span><span class="sxs-lookup"><span data-stu-id="65ee3-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="A variável CSS --theme-body-background realçada no painel Estilos" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="65ee3-170">A `--theme-body-background` variável CSS realçada no painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="65ee3-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="65ee3-171">Os problemas são automaticamente resolvidos por gravidade</span><span class="sxs-lookup"><span data-stu-id="65ee3-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="65ee3-172">A **ferramenta Issues** exibe recomendações para melhorar seu site, incluindo acessibilidade, desempenho, segurança e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="65ee3-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="65ee3-173">Com base em seus comentários, os problemas agora são automaticamente resolvidos por gravidade.</span><span class="sxs-lookup"><span data-stu-id="65ee3-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="65ee3-174">Em cada categoria de comentários, cada problema marcado como **Erro** aparece primeiro, seguido de cada problema marcado como Aviso **,** em seguida, cada problema marcado como uma **Dica**.</span><span class="sxs-lookup"><span data-stu-id="65ee3-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="65ee3-175">Para ajudá-lo a refinar seus problemas, as opções de filtro extra são planejadas para uma atualização futura.</span><span class="sxs-lookup"><span data-stu-id="65ee3-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="65ee3-176">Para obter mais informações sobre como revisar problemas, navegue até Encontrar e corrigir problemas com a ferramenta Problemas do [Microsoft Edge DevTools.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="65ee3-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="A ferramenta Issues exibe problemas organizados por gravidade" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="65ee3-178">A **ferramenta Issues** exibe problemas organizados por gravidade</span><span class="sxs-lookup"><span data-stu-id="65ee3-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="65ee3-179">Microsoft Edge Developer Tools for Visual Studio Code versão 1.1.7</span><span class="sxs-lookup"><span data-stu-id="65ee3-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="65ee3-180">O [Microsoft Edge Tools for Visual Studio Code versão][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] 1.1.7 fornece o DevTools do Microsoft Edge versão [88][DevtoolsWhatsNew202011Devtools].</span><span class="sxs-lookup"><span data-stu-id="65ee3-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="65ee3-181">Essa extensão agora suporta ARM dispositivos e não depende mais do [Depurador para a extensão do Microsoft Edge.][VisualstudioMarketplaceMsjsdiagDebuggerForEdge]</span><span class="sxs-lookup"><span data-stu-id="65ee3-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="65ee3-182">A versão 1.1.7 inclui as seguintes correções de bugs e melhorias.</span><span class="sxs-lookup"><span data-stu-id="65ee3-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="65ee3-183">Atualizou a confiabilidade do fechamento de destino.</span><span class="sxs-lookup"><span data-stu-id="65ee3-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="65ee3-184">Atualizou o painel lateral para atualizar automaticamente quando você depura destinos criados ou destruídos.</span><span class="sxs-lookup"><span data-stu-id="65ee3-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="65ee3-185">Adicionado um novo menu contextual que oferece acesso mais rápido às configurações de extensão e ao Changelog mais recente.</span><span class="sxs-lookup"><span data-stu-id="65ee3-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="65ee3-186">Atualizado e simplificado a versão da documentação de extensão, incluindo os recursos mais novos.</span><span class="sxs-lookup"><span data-stu-id="65ee3-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="65ee3-187">Para atualizar manualmente para a versão 1.1.7, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="65ee3-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="65ee3-188">Você pode registrar problemas e contribuir para a extensão no [repositório do GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="65ee3-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="65ee3-189">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="65ee3-189">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="65ee3-190">Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="65ee3-190">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="65ee3-191">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="65ee3-191">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="65ee3-192">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="65ee3-192">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Usando o DevTools em outros idiomas - Novidades no DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Novidades no DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools#css-variable-definitions-in-styles-pane "Definições de variável CSS no painel Estilos - Novidades no DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Novidades no DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Ferramentas de grupo juntas no Modo de Foco - Novidades no DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Abra o Menu de Comando - Execute comandos com o menu DevTools command do Microsoft Edge | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Alterar configurações de idioma do DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: /microsoft-edge/devtools-guide-chromium/service-workers/index "Melhorias do Service Worker | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: /microsoft-edge/progressive-web-apps-chromium/serviceworker#the-service-worker-lifecycle "O ciclo de vida do Trabalhador do Serviço - Use Os Trabalhadores do Serviço para gerenciar solicitações de rede e notificações por push | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: /microsoft-edge/progressive-web-apps-chromium/webappmanifests "Use o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao sistema operacional | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace de Extensões | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador do Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR1066604]: https://crbug.com/1066604 "Problema 1066604: DevTools: consulte detalhes sobre a instalação do ServiceWorker e ativação de eventos | Bugs do Chromium"  
[CR1136655]: https://crbug.com/1136655 "Problema 1136655: Devtools: Localização V2 | Bugs do Chromium"  
[CR1185945]: https://crbug.com/1185945 "Problema 1185945: Aviso de manifesto indica que todos os ícones devem ser quadrados | Bugs do Chromium"  
[CR1187735]: https://crbug.com/1187735 "Problema 1187735: Acessibilidade: MAS2.1.1: Teclado: Não é possível invocar a função 'Var(..)' usando o teclado | Bugs do Chromium"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propriedades personalizadas CSS (variáveis) | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Gerador de Imagens | PWABuilder"  

<!--  > [!NOTE]
> Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].  
> The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
-->