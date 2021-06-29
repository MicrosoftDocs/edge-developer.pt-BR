---
description: Sublinhados ondulados realçam problemas de código na ferramenta Elements, linha do tempo de atualização do serviço de trabalho e muito mais.
title: Novidades no DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 69fcd29f9b4cae9ec290798b767fbe54793cb2fd
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624777"
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

Na maioria das IDEs modernas, sublinhados ondulados em texto indicam erros de sintaxe.   Na Microsoft Edge versão 91 ou posterior, sublinhados ondulados são exibidos em HTML no visor **DOM** da **ferramenta Elements.**  Os sublinhados ondulados indicam problemas de código e sugestões relacionadas à acessibilidade, compatibilidade, desempenho e assim por diante.  Para obter mais informações sobre como revisar e editar problemas, navegue até [Encontrar e corrigir problemas usando a ferramenta Problemas.][DevtoolsIssuesIndex]  

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

Na Microsoft Edge versão 91 ou posterior, se você for um desenvolvedor do Progressive Web App ou do Service Worker, exibirá o ciclo de vida de atualização de seus Funcionários do Serviço como uma linha do tempo na ferramenta **Aplicativo.**  Esse recurso ajuda você a entender o tempo gasto pelo Trabalhador do Serviço em cada uma das etapas a seguir.  

*   **Install**  
*   **Wait**  
*   **Ativar**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Revise a Linha do Tempo no Ciclo de Atualizações do seu Trabalhador do Serviço" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Revise a **Linha do** Tempo no Ciclo **de Atualizações** do seu Trabalhador do Serviço  
:::image-end:::  

Para obter mais informações sobre o ciclo de vida dos Funcionários do Serviço, navegue até [o ciclo de vida do Trabalhador do Serviço.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]  Para obter mais informações sobre ferramentas de depuração para Aplicativos Web Progressivos e Funcionários de Serviço no DevTools, navegue até [Service Worker improvements][DevtoolsServiceWorkerIndex].  Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até o Problema [1066604][CR1066604].  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Os Aplicativos Web Progressivos não exibem mais avisos para ícones não quadrados  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

Na Microsoft Edge versão [90][DevtoolsWhatsNew202102Devtools] ou anterior, se o Manifesto do Aplicativo Web do seu PWA incluiu um ícone não quadrado, um aviso foi exibido na seção Erros e **Avisos** para cada ícone não quadrado.  Na Microsoft Edge versão 91 ou posterior, a seção **Manifesto** na ferramenta **Aplicativo** não exibirá avisos se você fornecer pelo menos um ícone quadrado.  Se você não fornecer ícones quadrados, um aviso exibirá a seguinte mensagem.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="Na Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         Na Microsoft Edge versão 90 ou anterior, um erro é exibido para cada ícone que não é quadrado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="Na Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         Na Microsoft Edge versão 91 ou posterior, nenhum erro é exibido quando você fornece pelo menos um ícone quadrado  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar erros e avisos em seu Manifesto do Aplicativo Web, navegue até a ferramenta **Aplicativo** e escolha a **seção Manifesto.**  Os erros e avisos estão listados no **título Erros e Avisos.**  Para obter mais informações sobre o Manifesto do Aplicativo Web, navegue até Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo [ao Sistema Operacional][ProgressiveWebAppsWebappmanifests].  Para criar ícones para incluir no Manifesto do Aplicativo Web, navegue até o Gerador de [Imagens do PWABuilder.][PwabuilderImagegenerator]  Para analisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [1185945][CR1185945].  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>O DevTools localizado agora tem suporte Chromium navegadores baseados em Chromium  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

A partir [Microsoft Edge versão 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools é exibido em seu próprio idioma.  Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code em seu idioma nativo, não apenas em inglês.  A equipe Microsoft Edge DevTools, a equipe chrome DevTools e a equipe do Google Lighthouse colaboraram para fornecer a mesma experiência em todos os navegadores Chromium baseados em Chromium.  Para obter mais informações sobre como usar o DevTools em seu idioma, navegue até Alterar configurações de idioma [do DevTools.][DevtoolsCustomizeLocalization]  Para obter mais informações sobre a colaboração nesse recurso no Chromium de código aberto, navegue até [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge navegador e DevTools definido como japonês" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Microsoft Edge navegador e DevTools definido como japonês  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Usar o teclado para navegar até variáveis CSS  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

A partir [Microsoft Edge versão 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], o painel **Estilos** exibe variáveis CSS e fornece um link diretamente para a definição de cada variável.  Na Microsoft Edge versão 91 ou posterior, você pode usar as teclas de seta para navegar facilmente para variáveis CSS.  Para abrir a definição no painel **Estilos,** passe o mouse em uma variável e selecione `Enter` .  Para obter mais informações sobre variáveis CSS, navegue até [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].  Para analisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [1187735][CR1187735].  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="A variável CSS --theme-body-background realçada no painel Estilos" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   A `--theme-body-background` variável CSS realçada no painel **Estilos**  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Os problemas são automaticamente resolvidos por gravidade  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

A **ferramenta Issues** exibe recomendações para melhorar seu site, incluindo acessibilidade, desempenho, segurança e assim por diante. Com base em seus comentários, os problemas agora são automaticamente resolvidos por gravidade.  Em cada categoria de comentários, cada problema marcado como **Erro** aparece primeiro, seguido de cada problema marcado como Aviso **,** em seguida, cada problema marcado como uma **Dica**.  Para ajudá-lo a refinar seus problemas, as opções de filtro extra são planejadas para uma atualização futura.  Para obter mais informações sobre como revisar problemas, navegue até [Encontrar e corrigir problemas usando a ferramenta Problemas.][DevtoolsIssuesIndex]  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="A ferramenta Issues exibe problemas organizados por gravidade" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   A **ferramenta Issues** exibe problemas organizados por gravidade  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Microsoft Edge Ferramentas de desenvolvedor Visual Studio Code versão 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

O [Microsoft Edge Ferramentas para Visual Studio Code versão][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] 1.1.7 fornece o DevTools do Microsoft Edge versão [88][DevtoolsWhatsNew202011Devtools].  Essa extensão agora suporta ARM dispositivos e não depende mais do [Depurador para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extensão.  A versão 1.1.7 inclui as seguintes correções de bugs e melhorias.  

*   Atualizou a confiabilidade do fechamento de destino.  
*   Atualizou o painel lateral para atualizar automaticamente quando você depura destinos criados ou destruídos.  
*   Adicionado um novo menu contextual que oferece acesso mais rápido às configurações de extensão e ao Changelog mais recente.  
*   Atualizado e simplificado a versão da documentação de extensão, incluindo os recursos mais novos.  
    
Para atualizar manualmente para a versão 1.1.7, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Você pode registrar problemas e contribuir para a extensão no [repositório do GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a>Visualizar o snap de rolagem CSS  

Agora você pode alternar o `scroll-snap` selo na ferramenta **Elements** para inspecionar o alinhamento de rolagem CSS.  Quando um elemento HTML em sua página da Web é aplicado a ela, um selo é exibido ao lado dele `scroll-snap-type` `scroll-snap` na ferramenta **Elements.**  Escolha o selo para ativar \(ou desativar\) a exibição de uma sobreposição de rolagem na página da Web.  Para analisar uma página da Web de exemplo, navegue até [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].  No exemplo, os pontos são exibidos em bordas de encaixe.  A porta de rolagem tem um contorno sólido enquanto os itens de encaixe têm estruturas de contorno.  O preenchimento de rolagem é preenchido em verde enquanto a margem de rolagem é preenchida em laranja.  Para revisar o histórico desse recurso no Chromium de código aberto, navegue até o Problema [862450][CR862450].  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS scroll-snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   CSS scroll-snap  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a>Nova ferramenta Inspetor de Memória  

Use a nova **ferramenta Inspetor de Memória** para inspecionar uma memória `ArrayBuffer` JavaScript e Wasm.  Abra a página da Web de demonstração Memória no [JS.][GlitchMemoryInspectorDemoJsHtml]  Na ferramenta **Fontes,** abra o `memory-write-wasm` arquivo e de definir um ponto de interrupção na linha `0x03c` .  Atualize a página da Web.  Expanda **a seção Escopo** no painel de depurador.  O novo ícone é exibido ao lado do **valor do buffer.**  Escolha-o para abrir a nova **ferramenta Inspetor de** Memória.  

Para saber mais sobre a depuração na ferramenta **Fontes,** navegue até Usando o [painel Depurador para depurar][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]código JavaScript .  Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1166577][CR1166577].  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Ferramenta Inspetor de Memória" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   **Ferramenta inspetor de** memória  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a>Novo painel de configurações do Selo na ferramenta Elements  

Agora, use as **configurações de** Selo na ferramenta **Elementos** para ativar \(ou desativar\) selos individuais.  Use esse recurso para personalizar e manter o foco em selos importantes enquanto você inspeciona páginas da Web.  Para exibir o painel de configurações de selo na parte superior da **ferramenta Elements,** conclua as seguintes ações.  

1.  Passe o mouse em qualquer elemento.  
1.  Abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Configurações de selo...**.  
    
Para exibir \(ou ocultar\) os selos, escolha \(ou remova\) a caixa de seleção ao lado do nome do selo.  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Painel de configurações de selo na ferramenta Elements" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   **Painel de configurações de** selo na **ferramenta Elements**  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a>Visualização de imagem aprimorada com informações de proporção  

As visualizações de imagem no DevTools foram aprimoradas para exibir mais informações, incluindo os detalhes a seguir.  

*   Tamanho renderizado  
*   Taxa de proporção renderizada  
*   Tamanho intrínseco  
*   Taxa de proporção intrínseco  
*   Tamanho do arquivo  
    
As informações ajudam você a entender melhor suas imagens e aplicar a otimização.  As informações da taxa de proporção de imagem também estão disponíveis na **ferramenta Rede,** quando você escolhe uma visualização de imagem.  

:::row:::
   :::column span="":::
      Na ferramenta **Elementos,** a visualização de imagem agora exibe mais informações sobre a imagem.  
   :::column-end:::
   :::column span="":::
      Além disso, as informações da taxa de proporção de imagem estão disponíveis na **ferramenta Rede,** quando você escolhe uma visualização de imagem.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Visualização de imagem com informações de proporção na ferramenta Elemento" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         Visualização de imagem com informações de proporção na **ferramenta Elemento**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Informações sobre a taxa de proporção de imagem na ferramenta Rede" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         Informações sobre a taxa de proporção de imagem na **ferramenta Rede**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problemas [1149832][CR1149832] e [1170656][CR1170656].  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a>Novas opções para configurar codificações de conteúdo na ferramenta Condições de rede 

Na ferramenta **Rede,** escolha o novo botão Mais condições de **rede...** ao lado do menu suspenso **Throttling** para abrir a **ferramenta Condições de** rede.  Para testar se as respostas do servidor estão codificadas corretamente para navegadores que não suportam [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]ou outro futuro, concluam `Content-Encoding` as seguintes ações.  

1.  Abra a **ferramenta Condições de** rede
1.  Navegue **até Codificações de**Conteúdo Aceito. 
1.  Remova a caixa de seleção ao lado `Content-Encoding` do que você deseja testar.  
    
Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1162042][CR1162042].  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Novas condições de rede mais... abre a ferramenta Condições de Rede para configurar a codificação de conteúdo" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   Novas **condições de rede... o botão** abre a ferramenta Condições **de** rede para configurar `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a>Aprimoramentos do painel de estilos  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a>Novo atalho para exibir o valor calculado no painel Estilos  

Agora, para exibir o valor CSS calculado no painel **Estilos,** conclua as seguintes ações.  

1.  Passe o mouse em uma propriedade CSS.  
1.  Abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Exibir valor calculado**.  
    
Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1076198][CR1076198].  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Novo atalho para exibir o valor calculado" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   Novo atalho para exibir o valor calculado  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a>Suporte para a palavra-chave accent-color  

A interface do usuário de preenchimento automático do painel **Estilos** agora detecta a palavra-chave CSS, que permite especificar a cor de destaque para controles de interface do usuário gerados `accent-color` pelo elemento.  Exemplos de controles de interface do usuário gerados por um elemento incluem caixas de seleção ou botões de rádio. Para obter mais informações sobre o status da implementação Chromium, navegue até Recurso: propriedade CSS de [cor de destaque.][ChromestatusFeature4752739957473280]  Para ativar esse recurso, navegue até e de definir a caixa de `edge://flags#enable-experimental-web-platform-features` seleção como **Habilitado**.  Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1092093][CR1092093].  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="Palavra-chave CSS de cor de destaque" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` Palavra-chave CSS
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a>Exibir detalhes sobre recursos bloqueados na exibição De detalhes do quadro  

Política de Permissões é uma API de plataforma web que oferece a um site a capacidade de permitir ou bloquear o uso de recursos do navegador em um quadro individual ou em um que `iframe` ele incorpora. Para obter mais informações, navegue até [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].  Para exibir os detalhes sobre por que um recurso é bloqueado, conclua as seguintes ações.  

1.  Navegue até [Política de Permissões OOPIF.][GlitchPermissionPolicyDemoMain]  
1.  Navegue até **a ferramenta Application.**  
1.  Escolha um quadro.  
1.  Navegue até a **seção Política de Permissões.**  
1.  Navegue até a **propriedade Disabled Features.**  
1.  Escolha **Mostrar detalhes**.  
1.  Escolha o ícone ao lado de cada política para navegar até a solicitação de rede `iframe` ou que bloqueou o recurso.  
    
Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Recursos bloqueados na exibição de detalhes do quadro" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   Recursos bloqueados na exibição de detalhes do quadro  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a>Filtrar experimentos na configuração Experimentos  

Encontre experimentos mais rápido com o novo filtro de experimento.  Por exemplo, para ativar novos experimentos para problemas de código, conclua as seguintes ações.
``

1.  Navegue **até Configurações**  >  **Experimentos**.  
1.  Navegue até a **caixa de texto** Filtro.  
1.  Digite `issues`.  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtrar experimentos na configuração Experimentos" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   Filtrar experimentos na **configuração Experimentos**  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a>Nova coluna Vary Header no painel de armazenamento de cache  

Use a nova `Vary Header` coluna no painel Cache **Armazenamento** para exibir os valores de cabeçalho de resposta [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP.  Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1186049][CR1186049].  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Coluna Vary Header" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   Coluna Vary Header  
:::image-end:::  

### <a name="sources-tool-improvements"></a>Melhorias da ferramenta Sources  

#### <a name="support-for-new-javascript-features"></a>Suporte para novos recursos JavaScript  

Agora, o DevTools suporta a nova marca privada verifica [a.k.a. #foo no][V8DevFeaturesPrivateBrandChecks] recurso de idioma JavaScript obj.  O recurso de verificações de marca privada estende o [operador in][MdnDocsWebJavascriptReferenceOperatorsIn] para dar suporte a campos de [classe privada][V8DevFeaturesClassFieldsPrivateClassFields] em um objeto específico.  Experimente nas ferramentas **Console** e **Sources.**  Além disso, para inspecionar os campos privados, conclua as seguintes ações.  

1.  Navegue até o painel **de depurador.**  
1.  Navegue até a **seção Escopo.**  
    
Para revisar o histórico desse recurso no Chromium de código aberto, navegue até o Problema [11374][CR11374].  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="Verificações de marca privada do JavaScript" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   Verificações de marca privada do JavaScript  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a>Suporte aprimorado para depuração de pontos de interrupção  

Os pacotes JavaScript modernos, como [Webpack][WebpackJsMain]e [Rollup,][RollupjsMain] suportam a divisão de código.  Para saber mais sobre a divisão de código, navegue até [Divisão de código][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].  Na Microsoft Edge versão 90 ou anterior, o DevTools apenas definirá pontos de interrupção em um único pacote.  Na Microsoft Edge versão 91 ou posterior, o DevTools define corretamente pontos de interrupção em vários pacotes quando você depura um componente compartilhado.  Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problemas [1142705][CR1142705], [979000][CR979000]e [1180794][CR1180794].  

#### <a name="support-hover-preview-with-bracket-notation"></a>Suporte à visualização de foco com notação de colchete  

O DevTools agora suporta a visualização de foco em expressões de membro JavaScript que usam `[]` a notação na **ferramenta Sources.**  Para analisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [1178305][CR1178305].  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Suporte à visualização de foco com notação []" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   Suporte à visualização de foco `[]` com notação  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a>Contorno aprimorado de arquivos HTML  

O DevTools agora tem melhor suporte de contorno para `.html` arquivos.  Na ferramenta **Fontes,** abra o `.html` arquivo.  Para ativar \(ou desativar\) o contorno de código, selecione em `Ctrl` + `Shift` + `O` Windows/Linux `Cmd` + `Shift` + `O` ou no macOS.  Na figura a seguir, o DevTools lista corretamente todas as funções no contorno.  Anteriormente, o DevTools exibia apenas algumas das funções.  Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problemas [761019][CR761019] e [1191465][CR1191465].  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Contorno aprimorado de arquivos HTML" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   Contorno aprimorado de arquivos HTML  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a>Rastreamentos de pilha de erros apropriados para depuração de Wasm  

Na Microsoft Edge versão 90 ou anterior, o DevTools exibia apenas referências genéricas de Wasm em Rastreamentos de pilha de erro.  Na Microsoft Edge versão 91 ou posterior, o DevTools resolve solicitações de função em linha e exibe o local de origem em Rastreamentos de pilha de erro para depuração de Wasm.  Para saber mais sobre Rastreamentos de pilha de erro no **Console,** navegue até [o erro][DevtoolsConsoleApiError].  

Na Microsoft Edge versão 91 ou posterior, o DevTools resolve solicitações de função em linha e exibe rastreamentos de pilha de erros apropriados para depuração de Wasm.  

:::row:::
   :::column span="":::
      Na Microsoft Edge versão 90 e anterior, o local de origem não é exibido nos rastreamentos de pilha error.  Os locais de origem incluem `dsquare` .  
   :::column-end:::
   :::column span="":::
      Na Microsoft Edge versão 91 e posterior, o local de origem é exibido nos rastreamentos de pilha error.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Rastreamentos de pilha de erros anteriores para depuração de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         Rastreamentos de pilha de erros apropriados para depuração de Wasm  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Rastreamentos de pilha de erros apropriados para depuração de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         Rastreamentos de pilha de erros apropriados para depuração de Wasm  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para analisar o histórico desse recurso no projeto Chromium de código aberto, navegue até Problema [1189161][CR1189161].  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

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
[DevtoolsIssuesIndex]: ../../../issues/index.md "Encontre e corrige problemas usando a ferramenta Problemas | Microsoft Docs"  
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

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Scroll Snap Demo | Glitch"  

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
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-91) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
