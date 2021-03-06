---
description: Emular deficiências de visão de cor, Doca para a esquerda no Menu de Comando e muito mais.
title: Novidades no DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 158d91e3d9c925beebe03a1baa8d6308b650262b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398942"
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

# <a name="whats-new-in-devtools-microsoft-edge-83"></a>Novidades no DevTools (Microsoft Edge 83)  

Seguindo a agenda atualizada do Chromium, estamos ajustando nossa agenda para as próximas versões do Microsoft Edge e cancelando a versão do Microsoft Edge 82. Confira nossa [postagem de blog][WindowsBlogStableRelease] para obter mais informações.  

Aqui estão os novos recursos disponíveis no DevTools no Microsoft Edge 83.  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Comunicados da equipe do Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.  Confira os comunicados para experimentar novos recursos no DevTools, no Microsoft Visual Studio Code e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a>Depurar remotamente o Microsoft Edge em dispositivos Windows 10  

O [aplicativo Ferramentas Remotas do Microsoft Edge \(Beta\)][RemoteTools] agora está disponível na [Microsoft Store][MicrosoftStore].  Usando este aplicativo, que estende o Portal de Dispositivos do [Windows][WindowsUwpDebugTestPerfDevicePortal], você pode se conectar da instância do Microsoft Edge em execução em sua máquina de desenvolvimento a um dispositivo Windows 10 remoto, exibir uma lista de destinos \(todas as guias no Microsoft Edge e [PWAs][ProgressiveWebAppsChromiumIndex] abertas no dispositivo Windows 10\) e usar o DevTools em sua máquina de desenvolvimento em um destino em execução no dispositivo Windows 10 remoto.  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="O aplicativo Ferramentas Remotas do Microsoft Edge (Beta) disponível na Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   O [aplicativo Ferramentas Remotas do Microsoft Edge (Beta)][RemoteTools] disponível na [Microsoft Store][MicrosoftStore]  
:::image-end:::  

[Leia nosso guia para configurar seu dispositivo Windows 10][DevtoolsRemoteDebuggingWindows]e sua máquina de desenvolvimento para depuração remota.  Deixe-nos saber sobre sua experiência de depuração remota [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

### <a name="new-ways-to-access-settings"></a>Novas maneiras de acessar Configurações  

Há várias configurações para o DevTools que você pode personalizar para fazer com que o DevTools pareça, sinta e trabalhe da maneira que você precisa. No Microsoft Edge 83, acessar [configurações][DevtoolsCustomizeIndexSettings] no DevTools agora é muito mais fácil.  Abra Configurações com o ícone de engrenagem ao lado de Alertas de Console e o menu principal.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="O ícone de engrenagem abre Configurações no DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   O ícone de engrenagem **abre Configurações** no DevTools  
:::image-end:::  

Você também pode abrir [Configurações][DevtoolsCustomizeIndexSettings] no **Menu Principal** em **Mais ferramentas.**

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu Principal > Mais ferramentas > Configurações" lightbox="../../media/2020/03/settings2.msft.png":::
   **Menu Principal**  >  **Mais ferramentas**  >  **Configurações**  
:::image-end:::  

Problema do Chromium [#1050855][CR1050855]

### <a name="new-and-improved-infobars"></a>Infobars novos e aprimorados

As barras de notificação informacional \(infobars\) no DevTools agora têm uma aparência aprimorada e mais funcionalidades. No Microsoft Edge 83, as barras de informações são mais fáceis de ler e fornecer botões para que você possa tomar a ação relevante imediatamente.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barra de informações para imprimir bastante um arquivo minificado no Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Barra de informações para imprimir bastante um arquivo minificado no Microsoft Edge Versão 83  
:::image-end:::  

Problema do Chromium [#1056348][CR1056348]

### <a name="navigate-the-color-picker-with-your-keyboard"></a>Navegue pelo Se picker de cores com o teclado  

O [Selador de][DevtoolsCssReferenceColorPicker] Cores é uma GUI no painel [Elementos][DevtoolsCssIndex] para alterações `color` e `background-color` declarações.  Nas versões anteriores do Microsoft Edge, você não era capaz de navegar na seção **Sombreamentos** do [Selador][DevtoolsCssReferenceColorPicker] de Cores com o teclado.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Agora você pode usar o teclado para mover o seletor na seção Sombreamentos do Seletor de Cores" lightbox="../../media/2020/03/color-picker.msft.png":::
   Agora você pode usar o teclado para mover o seletor na seção **Sombreamentos** do [Seletor de Cores][DevtoolsCssReferenceColorPicker]  
:::image-end:::  

No Microsoft Edge 83, agora você pode usar o teclado para mover o seletor na seção **Sombreamentos** do Seletor de Cores.  

Problema do Chromium [#963183][CR963183]  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a>A guia Propriedades agora é preenchida após uma atualização de página  

No Microsoft Edge 81 e anteriormente, a **guia Propriedades** no painel [Elementos][DevtoolsCssIndex] foi interrompida por atabas de página.  Quando você atualizeu a página, a **guia Propriedades** não preencheu as propriedades do elemento selecionado no momento.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="No Microsoft Edge 81 e anterior, a guia Propriedades ficou em branco após uma atualização de página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   No Microsoft Edge 81 e anterior, a guia **Propriedades** ficou em branco após uma atualização de página  
:::image-end:::  

No Microsoft Edge 83, agora você pode exibir as propriedades do elemento selecionado no momento após uma atualização de página na guia **Propriedades.**  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="No Microsoft Edge 83, a guia Propriedades exibe as propriedades do elemento selecionado no momento após uma atualização de página" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   No Microsoft Edge 83, a guia **Propriedades** exibe as propriedades do elemento selecionado no momento após uma atualização de página  
:::image-end:::  

Problema do Chromium [#1050999][CR1050999]  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a>Use as teclas de seta para rolar na ferramenta Alterações  

A **ferramenta Changes** rastreia todas as alterações feitas em CSS ou JavaScript no DevTools.  Você pode usar a ferramenta **Alterações para** exibir rapidamente todas as alterações e levá-los de volta ao seu editor/IDE.  

Para abrir a **ferramenta Alterações,** selecione `Ctrl` + `Shift` + `P` no DevTools para abrir o [Menu de Comando][DevToolsCommandMenuIndex] e digite `changes` .  escolha e execute o **comando Mostrar Alterações** para abrir a ferramenta **Alterações** na gaveta DevTools.  

Quando você fez uma alteração em um arquivo minificado, a ferramenta **Changes** permite que você role horizontalmente para exibir todo o código minificado.  A partir do Microsoft Edge 83, agora você pode rolar horizontalmente usando as teclas de seta no teclado.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de seta para exibir seu código minificado na ferramenta Alterações" lightbox="../../media/2020/03/changes.msft.png":::
   No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de seta para exibir as alterações feitas em seu código minificado na **ferramenta Alterações**  
:::image-end:::  

Se você usar leitores de tela ou o teclado para navegar [][PostTweetEdgeDevTools] ao redor do DevTools, envie seus comentários tuitando para nós ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 83 que contribuíram para o projeto Chromium de código aberto.  

### <a name="emulate-vision-deficiencies"></a>Emular deficiências visuais  

Abra a [guia Renderização][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] e use o novo recurso **emular** deficiências de visão para ter uma ideia melhor de como as pessoas com diferentes tipos de deficiências de visão experimentam seu site.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulando a visão desfocado" lightbox="../../media/2020/03/vision.msft.png":::
   Emulando a visão desfocado  
:::image-end:::  

O DevTools é capaz de emular a visão desfocado e os seguintes tipos de deficiências de visão [de cor.][ColorBlindnessTypes]  

| Deficiência de visão de cor | Detalhes |  
|:--- |:--- |  
| Protanopia | A incapacidade de perceber qualquer luz vermelha. |  
| Deuteranopia | A incapacidade de perceber qualquer luz verde. |  
| Tritanopia | A incapacidade de perceber qualquer luz azul. |  
| Achromatopsia | A incapacidade de perceber qualquer cor, exceto os tons de cinza \(extremamente raro\). |  

Existem versões menos extremas dessas deficiências de visão de cor e, na verdade, são mais comuns.  
Por exemplo, protanomaly é uma sensibilidade reduzida à luz vermelha (em vez de protanopia, que é a incapacidade completa de perceber a luz vermelha). No entanto, essas deficiências de visão **omaly** não são definidas claramente: cada pessoa com essa deficiência de visão é diferente e pode ver as coisas de forma diferente \(ser capaz de perceber mais/menos das cores relevantes\).  

Ao projetar para as simulações mais extremas no DevTools, seus aplicativos Web garantem estar acessíveis a pessoas com protanomaly, deuteranomaly, tritanomaly e achromatomaly também.  

Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#1003700][CR1003700]  

### <a name="emulate-locales"></a>Emular localidades  

Emular localidades definindo um local em **Sensor**  >  **Location**. [Abra o **Menu de Comando** ][DevToolsCommandMenuIndex] e digite para acessar a guia `Sensors` **Sensores.**  Depois de executar essas ações, o DevTools modifica a localidade padrão atual, afetando o código a seguir.  

*   `Intl.*` APIs, por exemplo: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Outras APIs JavaScript com conhecimento de localidade, `String.prototype.localeCompare` como e , por `*.prototype.toLocaleString` exemplo: `123_456..toLocaleString()`  
*   APIs DOM como `navigator.language` e `navigator.languages`  
*   O [cabeçalho de solicitação][MDNAcceptLanguage] HTTP de idioma aceito  

> [!NOTE]
> As atualizações `navigator.language` para e não ficam `navigator.languages` visíveis imediatamente, mas somente após a próxima atualização de página ou navegação.  As alterações no `Accept-Language` cabeçalho HTTP só são refletidas para solicitações subsequentes.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulando uma localidade" lightbox="../../media/2020/03/locale.msft.png":::
   Emulando uma localidade  
:::image-end:::  

Para experimentar uma demonstração, navegue até [Locale-dependent code example][MathiasByensLocaleDemo].

Problema do Chromium [#1051822][CR1051822]

### <a name="cross-origin-embedder-policy-coep-debugging"></a>Depuração de CoEP (Política de Embedder entre Origens)  

O painel Rede agora fornece informações de depuração de Política de [Embedder][COEP] entre Origens.  

A **coluna Status** agora fornece uma explicação rápida do motivo pelo qual uma solicitação foi bloqueada, bem como um link para exibir os headers dessa solicitação para depuração posterior:  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitações bloqueadas na coluna **Status**" lightbox="../../media/2020/03/status.msft.png":::
   Solicitações bloqueadas na **coluna Status**  
:::image-end:::  

A **seção Headers de** Resposta da guia **Headers** fornece mais orientações sobre como resolver os problemas:  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Mais orientações na seção Headers de Resposta" lightbox="../../media/2020/03/guidance.msft.png":::
   Mais orientações na seção **Headers de** Resposta  
:::image-end:::  

Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#1051466][CR1051466]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Novos ícones para pontos de interrupção, pontos de interrupção condicional e logpoints  

O painel Fontes tem novos ícones para pontos de interrupção, pontos de interrupção condicionais e pontos de log:  

*   Pontos de interrupção \(![Ponto de interrupção](../../media/2020/03/breakpoint.msft.png)\) são representados por círculos vermelhos.  
*   Pontos de interrupção condicionais \(![Ponto de interrupção condicional](../../media/2020/03/conditional.msft.png)\) são representados por círculos meio-brancos vermelhos.  
*   Logpoints \(![Logpoint](../../media/2020/03/logpoint.msft.png)\) são representados por círculos vermelhos com ícones de Console.  

A motivação para os novos ícones era tornar a interface do usuário mais consistente com outras ferramentas de depuração de GUI \(que normalmente são pontos de interrupção de cor vermelho\) e facilitar a distinção entre os três recursos rapidamente.  

Problema do Chromium [#1041830][CR1041830]  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a>Exibir solicitações de rede que configuram um caminho de cookie específico  

Use a nova `cookie-path` palavra-chave de filtro na **ferramenta Rede** para se concentrar nas solicitações de rede que definiram um caminho de [cookie específico.][MDNCookiePath]  

Confira [Solicitações de filtro por propriedades][DevtoolsNetworkReferenceFilterRequestsProperties] para descobrir mais palavras-chave como `cookie-path` .

### <a name="dock-to-left-from-the-command-menu"></a>Doca para a esquerda no Menu de Comando  

Abra o [Menu de Comando][DevToolsCommandMenuIndex] e execute o comando para mover `Dock to left` DevTools para a esquerda do seu viewport.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools encaixado à esquerda do viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   DevTools encaixado à esquerda do viewport  
:::image-end:::  

> [!NOTE]
> O **recurso Dock para a** esquerda está disponível desde o Microsoft Edge 75, mas anteriormente só era acessível no Menu [Principal][DevtoolsCustomizePlacementsChangeMainMenu].  O novo recurso no Microsoft Edge 83 é que agora você pode acessar esse recurso no Menu de Comando.  

Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#1011679][CR1011679]  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a>O painel Auditorias agora é o painel do Farol  

A equipe do DevTools frequentemente recebia comentários dos desenvolvedores da Web que, embora fosse possível executar [o Farol][GithubGoogleChromeLighthouse] do DevTools, ao experimentá-lo, eles não conseguiam encontrar o painel "Farol", portanto, o painel **Auditorias** agora é o painel **do Farol.**  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="O painel do Farol" lightbox="../../media/2020/03/lighthouse.msft.png":::
   O painel do Farol  
:::image-end:::  

> [!NOTE]
> O **painel do Farol** fornece links para conteúdo hospedado em sites de terceiros.  A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e os dados que eles podem coletar.  

### <a name="delete-all-local-overrides-in-a-folder"></a>Excluir todas as Substituições Locais em uma pasta  

Depois de **** configurar Substituições Locais, você pode passar o mouse em um diretório, abrir o menu contextual \(clique com o botão direito do mouse\) e escolha a nova opção **Excluir** todas as substituições locais para excluir todas as Substituições Locais nessa pasta.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Excluir todas as substituições" lightbox="../../media/2020/03/overrides.msft.png":::
   Excluir todas as substituições  
:::image-end:::  

Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#1016501][CR1016501]  

### <a name="updated-long-tasks-ui"></a>Interface do usuário de tarefas longas atualizadas  

Uma **Tarefa Longa** é um código JavaScript que monopoliza o thread principal por muito tempo, fazendo com que uma página da Web seja paralisada.  

Você foi capaz [][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] de visualizar tarefas longas no painel Desempenho há algum tempo, mas no Microsoft Edge 83 a interface do usuário de visualização de Tarefa Longa no painel Desempenho foi atualizada.  A parte Tarefa Longa de uma tarefa agora é colorida com um plano de fundo vermelho listrado.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="A nova interface do usuário de tarefa longa" lightbox="../../media/2020/03/long-task.msft.png":::
   A nova interface do usuário de tarefa longa  
:::image-end:::  

Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#1054447][CR1054447]  

### <a name="maskable-icon-support-in-the-manifest-pane"></a>Suporte a ícones mascaradas no painel Manifesto  

O Android Oreo introduziu ícones adaptáveis, que exibem ícones de aplicativo em uma variedade de formas em diferentes modelos de dispositivo.  **Ícones mascarados** são um novo formato de ícone que suporta ícones adaptáveis, o que permite garantir que o ícone [do PWA][ProgressiveWebAppsChromiumIndex] seja bom em dispositivos que suportam o padrão de ícones mascarados.  

Habilita a nova Caixa de seleção Mostrar apenas **** a área segura mínima para **ícones mascarados** no painel Manifesto para verificar se o ícone mascaral tem boa aparência em dispositivos Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Mostrar apenas a área segura mínima para a caixa de seleção ícones mascaradas" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   A caixa de seleção Mostrar apenas a área segura mínima para **ícones mascarados**  
:::image-end:::  

> [!NOTE]
> Esse recurso foi lançado no Microsoft Edge 81.  As atualizações abordadas aqui no Microsoft Edge 83 não foram abordadas no [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Novidades no DevTools (Microsoft Edge 81) | Microsoft Docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Alterar cores com o selador de cores | Microsoft Docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Começar a exibir e alterar o css | Microsoft Docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Alterar o posicionamento do menu principal | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Exibir a atividade de thread principal | Microsoft Docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho da renderização com a guia Renderização | Microsoft Docs"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web Progressivos no Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Começar com a depuração remota de dispositivos Windows 10 | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Pontos de interrupção de linha de código - Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitações por propriedades - Referência de análise de rede | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Visão geral do Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Ferramentas remotas para o Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Atualização em versões de canal estável para o Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo Problema - MicrosoftDocs/desenvolvedor de borda - GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  
[TheWebWeWant]: https://webwewant.fyi "A Web que queremos"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Tipos de Color Blindness"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemplo de código dependente de localidade"  

[CR963183]: https://crbug.com/963183 "Problema 963183: DevTools não são compatíveis com WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problema 1003700: Adicionar suporte ao DevTools para simulação de deficiência de visão colorida"  
[CR1011679]: https://crbug.com/1011679 "Problema 1011679: Introduzir 'Encaixe para a Esquerda' usando o Menu de Comando"  
[CR1016501]: https://crbug.com/1016501 "Problema 1016501: Solicitação de Recurso: Botão para excluir todas as substituições locais"  
[CR1050999]: https://crbug.com/1050999 "Problema 1050999: Guia Propriedades"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: Suporte à depuração DE COOP/COEP no DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problema 1054447: Atualizar métricas de desempenho na Linha do Tempo do DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: adicionar interface do usuário para emular localidade"
[CR1041830]: https://crbug.com/1041830 "Problema 1041830: Melhorar as cores para pontos de interrupção"
[CR1050855]: https://crbug.com/1050855 "Problema 1050855: a exibição de configurações é difícil de descobrir"
[CR1056348]: https://crbug.com/1056348 "Problema 1056348: Atualização do componente infobar"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP e COEP explicados - Política de abridor entre origens"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP e COEP explicados - Política de embedder entre origens"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "| GitHub"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/updates/2020/03/devtools/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
