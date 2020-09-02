---
title: O que há de novo no DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4f155a99d28d208bc288e3175b49c221684619a0
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991198"
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

# O que há de novo no DevTools (Microsoft Edge 80)  

## Anúncios da equipe do Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools! Dê uma olhada neles para experimentar os novos recursos do DevTools, as extensões de código do VS e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### Melhorias de acessibilidade no DevTools  

A equipe do DevTools contribuiu com as mudanças do 170 para o Chromium para solucionar problemas de cor de alto impacto, teclado e leitor de tela no DevTools.  Cada desenvolvedor que cria a Web deve poder usar o DevTools.  

> ##### Figura 1  
> A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela  
> ![A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela][ImagePerformanceToolKeyboardReaderImprovements]  

Deseja saber como tornar sua página da Web acessível a todos os seus usuários?  Baixe as [informações sobre acessibilidade][AccessibilityInsights] e as extensões [webhint][WebhintBrowserExtension] para o Microsoft Edge para começar.  

Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !  

Chromium problema [#963183][crbug963183]  

### Usando o DevTools em outros idiomas  

Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e código VS, em seu idioma nativo, não apenas em inglês.  Estamos entusiasmados a anunciar a localização do DevTools, que agora você pode usar em um dos dez idiomas além do inglês:  

:::row:::
   :::column span="":::
      Chinês \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chinês \ (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Francês – Fran-Fran&#231;ais
   :::column-end:::
   :::column span="":::
      Alemão – Deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italiano-Italiano
   :::column-end:::
   :::column span="":::
       &#26085;&#26412;&#35486; japonês
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Coreano- &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Português-Portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Russo –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Espanhol-espa&#241;ol
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

Navegue até `edge://flags` e defina o sinalizador **habilitar ferramentas para desenvolvedores localizados** como **habilitado**.  Defina também o sinalizador de **experimentos das ferramentas de desenvolvedor** como **habilitado**.  Reinicie o Microsoft Edge e abra o DevTools.  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  O DevTools corresponde ao idioma usado para o Microsoft Edge `edge://settings/languages` .  

> ##### Figura 2  
> O DevTools em alemão  
> ![O DevTools em alemão][ImageLocalizedGerman]  

Se você quiser usar o DevTools em um idioma diferente daqueles que estão disponíveis, [tweet][PostTweetEdgeDevTools] conosco ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) .  

Chromium problema [#941561][crbug941561]  

### extensão do Microsoft Edge da WebDicas  

A extensão WebDicas da Microsoft Edge permite que você examine facilmente sua página da Web e obtenha comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.  Leia mais em [https://webhint.io][Webhint] .  

> ##### Figura 3  
> A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada  
> ![A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada][ImageHintsTabWebhintExtension]  

[Experimente a extensão do navegador da webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].  Depois de instalar a extensão, abra a DevTools e selecione a guia dicas.  Aqui, execute uma verificação de site personalizável.  Vá para [webhint.Io][WebhintBrowserExtension] para saber mais.

### Modo de exibição 3D  

Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do [modelo de objeto de documento \ (dom \)][MDNDocumentObjectModel] ou do contexto de empilhamento de [índice z][MDNZIndex] .  

> ##### Figura 4  
> O modo de exibição 3D no DevTools  
> ![O modo de exibição 3D no DevTools][Image3DView]  

Para acessar o modo de exibição 3D, navegue até `edge://flags` e assegure-se de que o sinalizador de **experimentos das ferramentas de desenvolvedor** esteja definido como **habilitado**.  Reinicie o Microsoft Edge e abra o DevTools.  Pressione `F1` na seção devtools ou vá para **configurações**, navegue até **experimentos** e marque a caixa de seleção **habilitar modo de exibição 3D** .  Agora, pressione `Ctrl`  +  `Shift`  +  `P` , digite o **modo de exibição 3D** e selecione **Mostrar modo de exibição 3D**.  

Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao modo de exibição 3D para nos enviar seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).  

Chromium problema [#987787][crbug987787]

### Extensões de código do Visual Studio  

A equipe do DevTools também lançou algumas extensões para o [código do Visual Studio \ (vs Code \)][VisualStudioCode] que permitem que você use o poder do devtools diretamente do seu editor de texto! Confira as extensões abaixo:  

#### Elementos do Microsoft Edge  

Use a ferramenta de elementos de dentro do código VS adicionando os [elementos para Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs extensão de código.  

> ##### Figura 5  
> A ferramenta elementos no código VS usando os elementos da extensão do Microsoft Edge  
> ![A ferramenta elementos no código VS usando os elementos da extensão do Microsoft Edge][ImageElementsVisualStudioCode]  

Para obter mais informações, confira [elementos para o Microsoft Edge vs extensão de código][VisualStudioCodeElementEdgeExtension].  

#### Depurador para Microsoft Edge  

Com o [depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs extensão de código, depure o JavaScript executando no Microsoft Edge diretamente de um código vs!  

> ##### Figura 6  
> O depurador para extensão do Microsoft Edge no código VS  
> ![O depurador para extensão do Microsoft Edge no código VS][ImageDebuggerExtensionVisualStudioCode]  

Para obter mais informações, confira [como depurar o Microsoft Edge a partir de código vs][VisualStudioCodeDebuggerEdgeExtension].  

#### Dica da web  

A extensão de código do [webhint][VisualStudioMarketplaceWebhintExtension] vs usa `webhint` para melhorar sua página da Web enquanto você está escrevendo! Esta extensão executa e relata os diagnósticos nos arquivos do espaço de trabalho com base na `webhint` análise.  

> ##### Figura 7  
> A extensão de código do webhint x que analisa um arquivo. TSX no código VS  
> ![A extensão de código do webhint x que analisa um arquivo. TSX no código VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

[Saiba mais sobre a extensão de WebDicas de código vs][WebhintVisualStudioCodeExtension].  

### Integração do Visual Studio
No Visual Studio 2019 versão 16,2 ou posterior, use o depurador do Visual Studio para Depurar JavaScript em execução no Microsoft Edge.  [Baixe o Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso.  

> ##### Figura 8  
> O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta  
> ![O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta][ImageVisualStudioLaunchWebApp]  

[Leia nossa postagem no blog para saber como depurar o Microsoft Edge do Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].  

### Rastrear mensagens do console de prevenção  

A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você contra acompanhamento de sites que ainda não visitou.  A configuração de prevenção de rastreamento padrão é o modo balanceado, que bloqueia os rastreadores de terceiros e os rastreadores mal-intencionados conhecidos para obter uma experiência que equilibre a compatibilidade com a privacidade e a compatibilidade com a Web.  Para fornecer a você mais informações sobre a compatibilidade de sua página da Web quando determinados rastreadores estão bloqueados, também adicionamos mensagens de aviso no console quando um controlador é bloqueado.  

> ##### Figura 9  
> Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador  
> ![Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador][ImageTrackingPrevention]  

[Leia mais sobre a prevenção de rastreamento e o equilíbrio entre a compatibilidade entre privacidade e Web][TrackingPrevention].  

## Anúncios do projeto Chromium  

As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 80 que contribuíram para o projeto de código-fonte aberto Chromium.  

### Suporte a redeclaraçãos Let e Class no console  

O console agora oferece suporte a redeclarações `let` e `class` instruções.  A incapacidade de redeclarar foi um aborrecimento comum para desenvolvedores da Web que usam o console para experimentar com o novo código JavaScript.  

> [!WARNING]
> A redeclaração de uma `let` `class` instrução ou de uma instrução em um script fora do console ou dentro de uma única entrada de console ainda causa uma `SyntaxError` .  

Por exemplo, anteriormente, ao redeclarar uma variável local com `let` , o console emitiu um erro:  

> ##### Figura 10  
> O console no Microsoft Edge 79 mostrando que a redeclaração Let falha  
> ![O console no Microsoft Edge 79 mostrando que a redeclaração Let falha][ImageConsoleRedeclarationFails]  

Agora, o console permite a redeclaração:  

> ##### Figura 11  
> O console no Microsoft Edge 80 mostrando que a redeclaração permite que a redeclaração seja bem-sucedida  
> ![O console no Microsoft Edge 80 mostrando que a redeclaração permite que a redeclaração seja bem-sucedida][ImageConsoleRedeclarationSucceeds]  

Chromium problema [#1004193][crbug1004193]  

### Depuração de Webassembly aprimorada  

DevTools começou a dar suporte ao [padrão de depuração Dwarf][DwarfHome], o que significa maior suporte para a depuração de código, a definição de pontos de interrupção e a resolução de rastreamentos de pilha em seus idiomas de origem no devtools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### Atualizações do painel de rede  

#### Solicitar cadeias do iniciador na guia iniciador  

Agora você pode ver os iniciadores e as dependências de uma solicitação de rede como uma lista aninhada.  Isso pode ajudá-lo a entender por que um recurso foi solicitado ou de qual atividade de rede um determinado recurso \ (por exemplo, um script \) causou.  

> ##### Figura 12  
> Uma cadeia de iniciador de solicitações na guia iniciador  
> ![Uma cadeia de iniciador de solicitações na guia iniciador][ImageRequestInitiatorChain]  

Depois de [registrar a atividade de rede no painel de rede][DevToolsNetworkIndex], clique em um recurso e, em seguida, vá para a guia **iniciador** para ver a **cadeia do iniciador de solicitações**:  

*   O **recurso inspecionado** está em negrito.  Na captura de tela acima, `ai.2.min.js` é o recurso inspecionado.  
*   Os recursos acima do recurso inspecionado são os **iniciadores**.  Na captura de tela acima, `https://www.microsoftedgeinsider.com` é o iniciador de `ai.2.min.js` .  Em outras palavras, `https://www.microsoftedgeinsider.com` causou a solicitação de rede `ai.2.min.js` .  
*   Os recursos abaixo do recurso inspecionado são as **dependências**.  Na captura de tela acima, `https://dc.services.visualstudio.com/v2/track` é uma dependência de `ai.2.min.js` .  Em outras palavras, `ai.2.min.js` causou a solicitação de rede `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> As informações de dependência e de iniciador também podem ser acessadas mantendo `Shift` e passando o mouse sobre os recursos de rede.  Consulte [Exibir iniciadores e dependências][DevToolsNetworkReferenceViewInitiatorsDependencies].  

Chromium problema [#842488][crbug842488]  

#### Realçar a solicitação de rede selecionada na visão geral  

Depois de clicar em um recurso de rede para inspecioná-lo, o painel de rede agora coloca uma borda azul ao meio do recurso na **visão geral**.  Isso pode ajudá-lo a detectar se a solicitação de rede está acontecendo antes ou depois do esperado.  

> ##### Figura 13  
> O painel Visão geral destacando o recurso inspecionado  
> ![O painel Visão geral destacando o recurso inspecionado][ImageOverviewPaneInspectedResource]  

Chromium problema [#988253][crbug988253]  

#### Colunas URL e caminho no painel rede  

Use as colunas novo **caminho** e **URL** no painel **rede** para ver o caminho absoluto ou a URL completa de cada recurso de rede.  

> ##### Figura 14  
> As colunas novo caminho e URL no painel de rede  
> ![As colunas novo caminho e URL no painel de rede][ImagePathNetworkPanel]  

Clique com o botão direito do mouse no cabeçalho da tabela de **cascata** e selecione **caminho** ou **URL** para mostrar as novas colunas.  

Chromium problema [#993366][crbug993366]  

#### Cadeias de agente do usuário atualizadas  

O DevTools dá suporte à configuração de uma cadeia de caracteres de agente de usuário personalizada por meio da guia **condições de rede** .  A cadeia de caracteres do agente do usuário afeta o `User-Agent` cabeçalho http anexado aos recursos de rede e também o valor de `navigator.userAgent` .  

As cadeias de caracteres de agente do usuário predefinidos foram atualizadas para refletir versões modernas do navegador.  

> ##### Figura 15  
> O menu do agente do usuário na guia condições de rede  
> ![O menu do agente do usuário na guia condições de rede][ImageUserAgentNetworkConditionsTab]  

Para acessar as **condições da rede**, [abra o menu de comando][DevToolsCommandMenuIndex] e execute o `Show Network Conditions` comando.  

> [!NOTE]
> Você também pode [definir cadeias de caracteres de agente do usuário no modo de dispositivo][DevToolsDeviceModeIndex].  

Chromium problema [#1029031][crbug1029031]  

### Atualizações do painel auditorias  

#### Nova interface do usuário de configuração  

A interface do usuário de configuração tem um design novo e responsivo, e as opções de configuração de limitação foram simplificadas.  Consulte [limitação do painel de auditoria][GitHubGoogleChromeDevToolsAuditsPanelThrottling] para obter mais informações sobre as alterações na interface do usuário de limitação.  

> ##### Figura 16  
> A nova interface do usuário de configuração  
> ![A nova interface do usuário de configuração][ImageConfigurationUI]  

### Atualizações da guia cobertura  

#### Modos de cobertura per-Function ou per-Block  

A [guia cobertura][DevToolsCoverageIndex] tem um novo menu suspenso que permite especificar se os dados da cobertura de código devem ser coletados **por função** ou **por bloco**.  A cobertura **por bloco** é mais detalhada, mas também muito mais cara para coletar.  O DevTools usa a cobertura **por função** por padrão agora.  

> [!CAUTION]
> Você pode ver diferenças em grandes coberturas de código em arquivos HTML, dependendo se você usa o modo **por função** ou **por bloqueio** .  Ao usar o modo **por função** , scripts embutidos em arquivos HTML são tratados como funções.  Se o script for executado de forma alguma, o DevTools marcará todo o script como código usado.  Somente se o script não for executado, o DevTools marcará o script como código não usado.  

> ##### Figura 17  
> O menu suspenso modo de cobertura  
> ![O menu suspenso modo de cobertura][ImageCoverageMode]  

#### A cobertura agora deve ser iniciada por uma recarga de página  

A alternância da cobertura de código sem um recarregamento de página foi removida porque os dados de cobertura não eram confiáveis.  Por exemplo, uma função pode ser reportada como não usada se o tempo de execução era muito demorado e o coletor de lixo V8 o limpou.  

Chromium problema [#1004203][crbug1004203]  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge DevTools equipe  

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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2019/12/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
