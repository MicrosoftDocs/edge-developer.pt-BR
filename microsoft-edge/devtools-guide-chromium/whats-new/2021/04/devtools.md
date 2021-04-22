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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a>Novidades no DevTools (Microsoft Edge 91)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a>Sublinhados ondulados realçam problemas de código e melhorias na ferramenta Elements  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

Na maioria das IDEs modernas, sublinhados ondulados em texto indicam erros de sintaxe.   No Microsoft Edge versão 91 ou posterior, sublinhados ondulados são exibidos em HTML na exibição **DOM** da **ferramenta Elements.**  Os sublinhados ondulados indicam problemas de código e sugestões relacionadas à acessibilidade, compatibilidade, desempenho e assim por diante.  Para obter mais informações sobre como revisar e editar problemas, navegue até Encontrar e corrigir problemas com a ferramenta Problemas do [Microsoft Edge DevTools][DevtoolsIssuesIndex].  

Para abrir a **ferramenta Problemas** e saber mais sobre o problema e como corrigi-lo, conclua uma das seguintes ações.  

*   Selecione e segure `Shift` e escolha qualquer sublinhado ondulado.  
*   Conclua as seguintes ações.  
    1.  Passe o mouse em qualquer sublinhado ondulado.  
    1.  Abra o menu contextual \(clique com o botão direito do mouse\).  
    1.  Escolha **Mostrar em Problemas**.  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Escolha o erro sublinhado na ferramenta Elements" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         Escolha o erro sublinhado na **ferramenta Elements**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Exibir detalhes de erro na ferramenta Problemas" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         Exibir detalhes de erro na ferramenta **Problemas**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Saiba mais sobre o DevTools com dicas de ferramentas informativas  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

O recurso Dicas de Ferramentas do DevTools ajuda você a aprender sobre todas as diferentes ferramentas e painéis no DevTools.  Para desativar dicas de ferramenta, selecione `Esc` .  Para ativar dicas de ferramenta, conclua uma das seguintes ações.  

*   Selecione `Ctrl` + `Shift` + `H` \(Windows/Linux\) ou `Cmd` + `Shift` + `H` \(macOS\).  
*   [Abra o Menu de Comando][DevtoolsCommandMenuIndexOpenCommandMenu] e digite `tooltips` .  
*   Escolha **Personalizar e controlar o DevTools** \( \) > Ajuda Para alternar as dicas de ferramenta `...` ****  >  **DevTools**.  

Além disso, se você ativar o experimento Modo de Foco e Dicas de Ferramentas [do DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] também poderá escolher o botão Alternar as Dicas de Ferramentas **de DevTools** \( \) na parte inferior da Barra de `?` **Atividades**.  

Para exibir mais informações sobre como usar o DevTools, a turn on Tooltips e, em seguida, passe o mouse em cada região descrita do DevTools.  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Passe o mouse em qualquer lugar na região realçada da ferramenta Problemas para exibir mais detalhes" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   Passe o mouse em qualquer lugar na região realçada da **ferramenta Problemas** para exibir mais detalhes  
:::image-end:::  

## <a name="service-worker-update-timeline"></a>Linha do tempo de atualização do trabalhador do serviço  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

No Microsoft Edge versão 91 ou posterior, se você for um desenvolvedor do Progressive Web App ou Service Worker, poderá exibir o ciclo de vida de atualização de seus Funcionários do Serviço como uma linha do tempo na ferramenta **Aplicativo.**  Esse recurso ajuda você a entender o tempo gasto pelo Trabalhador do Serviço em cada uma das etapas a seguir.  

*   **Install**  
*   **Wait**  
*   **Ativar**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Revise a Linha do Tempo no Ciclo de Atualizações do seu Trabalhador do Serviço" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Revise a **Linha do** Tempo no Ciclo **de Atualizações** do seu Trabalhador do Serviço  
:::image-end:::  

Para obter mais informações sobre o ciclo de vida dos Funcionários do Serviço, navegue até [o ciclo de vida do Trabalhador do Serviço.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]  Para obter mais informações sobre ferramentas de depuração para Aplicativos Web Progressivos e Funcionários de Serviço no DevTools, navegue até [Service Worker improvements][DevtoolsServiceWorkerIndex].  Para revisar atualizações em tempo real sobre esse recurso no projeto de código aberto do Chromium, navegue até o Problema [1066604][CR1066604].  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Os Aplicativos Web Progressivos não exibem mais avisos para ícones não quadrados  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

No Microsoft Edge versão [90][DevtoolsWhatsNew202102Devtools] ou anterior, se você incluiu um ícone não quadrado no Manifesto do Aplicativo Web do seu PWA, a seção **Manifesto** na ferramenta **Aplicativo** exibiu um aviso em Erros e **Avisos** para cada ícone não quadrado.  No Microsoft Edge versão 91 ou posterior, a seção **Manifesto** na ferramenta **Aplicativo** não exibirá avisos se você fornecer pelo menos um ícone quadrado.  Se você não fornecer ícones quadrados, um aviso exibirá a seguinte mensagem.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="No Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         No Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="No Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         No Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar erros e avisos em seu Manifesto do Aplicativo Web, navegue até a ferramenta **Aplicativo** e escolha a **seção Manifesto.**  Os erros e avisos estão listados no **título Erros e Avisos.**  Para obter mais informações sobre o Manifesto do Aplicativo Web, navegue até Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo [ao Sistema Operacional][ProgressiveWebAppsWebappmanifests].  Para criar ícones para incluir no Manifesto do Aplicativo Web, navegue até o Gerador de [Imagens do PWABuilder.][PwabuilderImagegenerator]  Para revisar atualizações em tempo real sobre esse recurso no projeto de código aberto do Chromium, navegue até o Problema [1185945][CR1185945].  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>DevTools localizado agora tem suporte em navegadores baseados em Chromium  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

A partir [do Microsoft Edge versão 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], o Microsoft Edge DevTools é exibido em seu próprio idioma.  Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code em seu idioma nativo, não apenas em inglês.  A equipe do Microsoft Edge DevTools, a equipe do Chrome DevTools e a equipe do Google Lighthouse colaboraram para fornecer a mesma experiência em todos os navegadores baseados em Chromium.  Para obter mais informações sobre como usar o DevTools em seu idioma, navegue até Alterar configurações de idioma [do DevTools.][DevtoolsCustomizeLocalization]  Para obter mais informações sobre a colaboração neste recurso no projeto de código aberto do Chromium, navegue até [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Navegador do Microsoft Edge e DevTools definido como japonês" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Navegador do Microsoft Edge e DevTools definido como japonês  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Usar o teclado para navegar até variáveis CSS  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

A partir [do Microsoft Edge versão 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], o painel **Estilos** exibe variáveis CSS e fornece um link diretamente para a definição de cada variável.  No Microsoft Edge versão 91 ou posterior, você pode usar as teclas de seta para navegar facilmente para variáveis CSS.  Para abrir a definição no painel **Estilos,** passe o mouse em uma variável e selecione `Enter` .  Para obter mais informações sobre variáveis CSS, navegue até [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].  Para revisar atualizações em tempo real sobre esse recurso no projeto de código aberto do Chromium, navegue até o Problema [1187735][CR1187735].  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="A variável CSS --theme-body-background realçada no painel Estilos" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   A `--theme-body-background` variável CSS realçada no painel **Estilos**  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Os problemas são automaticamente resolvidos por gravidade  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

A **ferramenta Issues** exibe recomendações para melhorar seu site, incluindo acessibilidade, desempenho, segurança e assim por diante. Com base em seus comentários, os problemas agora são automaticamente resolvidos por gravidade.  Em cada categoria de comentários, cada problema marcado como **Erro** aparece primeiro, seguido de cada problema marcado como Aviso **,** em seguida, cada problema marcado como uma **Dica**.  Para ajudá-lo a refinar seus problemas, as opções de filtro extra são planejadas para uma atualização futura.  Para obter mais informações sobre como revisar problemas, navegue até Encontrar e corrigir problemas com a ferramenta Problemas do [Microsoft Edge DevTools.][DevtoolsIssuesIndex]  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="A ferramenta Issues exibe problemas organizados por gravidade" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   A **ferramenta Issues** exibe problemas organizados por gravidade  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Microsoft Edge Developer Tools for Visual Studio Code versão 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

O [Microsoft Edge Tools for Visual Studio Code versão][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] 1.1.7 fornece o DevTools do Microsoft Edge versão [88][DevtoolsWhatsNew202011Devtools].  Essa extensão agora suporta ARM dispositivos e não depende mais do [Depurador para a extensão do Microsoft Edge.][VisualstudioMarketplaceMsjsdiagDebuggerForEdge]  A versão 1.1.7 inclui as seguintes correções de bugs e melhorias.  

*   Atualizou a confiabilidade do fechamento de destino.  
*   Atualizou o painel lateral para atualizar automaticamente quando você depura destinos criados ou destruídos.  
*   Adicionado um novo menu contextual que oferece acesso mais rápido às configurações de extensão e ao Changelog mais recente.  
*   Atualizado e simplificado a versão da documentação de extensão, incluindo os recursos mais novos.  
    
Para atualizar manualmente para a versão 1.1.7, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Você pode registrar problemas e contribuir para a extensão no [repositório do GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

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
