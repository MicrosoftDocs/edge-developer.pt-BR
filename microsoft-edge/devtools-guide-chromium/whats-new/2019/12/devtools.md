---
description: Melhorias de acessibilidade, uso do DevTools em outros idiomas e muito mais.
title: Novidades no DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 58e5bf43720c7ba94a721804eb44d82ba657b599
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564991"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a>Novidades no DevTools (Microsoft Edge 80)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Comunicados da equipe Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe Microsoft Edge DevTools.  Confira os comunicados para experimentar novos recursos no DevTools, Microsoft Visual Studio Extensões de Código e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais Microsoft Edge [de][MicrosoftEdgePreviewChannels] visualização e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### <a name="accessibility-improvements-to-the-devtools"></a>Melhorias de acessibilidade no DevTools  

A equipe do DevTools contribuiu com 170 alterações no Chromium para resolver problemas de contraste de cores de alto impacto, teclado e leitor de tela no DevTools.  Cada desenvolvedor que está criando a Web deve ser capaz de usar o DevTools.  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="A ferramenta Performance no DevTools com as melhorias de navegação de teclado e leitor de tela" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   A **ferramenta Performance** no DevTools com as melhorias de navegação de teclado e leitor de tela  
:::image-end:::  

Quer saber como tornar sua página da Web acessível para todos os usuários?  Baixe os [Insights de Acessibilidade][AccessibilityInsights] e [extensões webhint][WebhintBrowserExtension] para Microsoft Edge para começar.  

Se você usar leitores de tela ou o teclado para navegar [][PostTweetEdgeDevTools] ao redor do DevTools, envie seus comentários tuitando para nós ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium problema [#963183][CR963183]  

### <a name="using-the-devtools-in-other-languages"></a>Usando o DevTools em outros idiomas  

Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como StackOverflow e Visual Studio Code, em seu idioma nativo, não apenas em inglês.  Estamos animados para anunciar a localização para o DevTools, que agora você pode usar em um dos 10 idiomas além do inglês:  

:::row:::
   :::column span="":::
      Chinês \(Simplificado\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chinês \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Francês –&#231;ais
   :::column-end:::
   :::column span="":::
      Alemão - deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italiano - italiano
   :::column-end:::
   :::column span="":::
      Japonês - &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Coreano - &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Português - portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Russo – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Espanhol - espa&#241;ol
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

Navegue `edge://flags` até e de definir o sinalizador **Habilitar ferramentas de desenvolvedor localizadas** **como Habilitado**.  Também de definir o **sinalizador de experimentos de Ferramentas de** Desenvolvedor como **Habilitado**.  Reinicie Microsoft Edge e abra o DevTools.  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  Os DevTools combinam com o idioma que você usa para Microsoft Edge em `edge://settings/languages` .  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   O DevTools em alemão  
:::image-end:::  

Se você quiser usar o DevTools em um idioma diferente dos que estão disponíveis, [tweet][PostTweetEdgeDevTools] para nós ou escolha o [ícone Enviar Comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium problema [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>webhint Microsoft Edge extensão  

A extensão webhint Microsoft Edge permite que você digitalizar facilmente sua página da Web e obter comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.  Leia mais em [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="A ferramenta Hints no DevTools quando a extensão do navegador webhint é instalada" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   A **ferramenta Hints** no DevTools quando a extensão do navegador webhint é instalada  
:::image-end:::  

[Experimente a extensão do navegador webhint em Microsoft Edge][MicrosoftEdgeInsiderAddons].  Depois de instalar a extensão, abra o DevTools e escolha a **ferramenta Dicas.**  A partir daqui, execute uma verificação de site personalizável.  Vá até [webhint.io][WebhintBrowserExtension] para saber mais.

### <a name="3d-view"></a>Modo de exibição 3D  

Use o **View 3D** para depurar seu aplicativo Web navegando pelo modelo de objeto de documento [\(DOM\)][MDNDocumentObjectModel] ou o contexto de empilhamento [de índice z.][MDNZIndex]  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="A exibição 3D no DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   A **exibição 3D** no DevTools  
:::image-end:::  

Para acessar o Modo de Exibição 3D, navegue até e verifique se o sinalizador de experimentos de Ferramentas de Desenvolvedor está `edge://flags` definido como **Habilitado**. ****  Reinicie Microsoft Edge e abra o DevTools.  Selecione na seção DevTools ou abra a seção Configurações Experimentos e ative a caixa de seleção Habilitar o Modo de `F1` ****  >  **** Exibição **3D.**  Agora, selecione `Ctrl`  +  `Shift`  +  `P` , digite em **Exibição 3D** e selecione **Mostrar Exibição 3D**.  

Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao Modo de Exibição 3D, portanto, envie seus [comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium problema [#987787][CR987787]

### <a name="visual-studio-code-extensions"></a>Visual Studio Code extensões  

A equipe do DevTools também [][VisualStudioCode] lançou algumas extensões para Visual Studio Code que permitem que você use o poder do DevTools diretamente do editor de texto. Confira as seguintes extensões.  

#### <a name="elements-for-microsoft-edge"></a>Elementos para Microsoft Edge  

Use a ferramenta Elements de dentro Visual Studio Code adicionando a extensão [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="A ferramenta Elements no Visual Studio Code usando os elementos para Microsoft Edge extensão" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   A **ferramenta Elements** no Visual Studio Code usando os elementos para Microsoft Edge extensão  
:::image-end:::  

Para obter mais informações, confira [Elementos para Microsoft Edge Visual Studio Code extensão][VisualStudioCodeElementEdgeExtension].  

#### <a name="debugger-for-microsoft-edge"></a>Depurador para Microsoft Edge  

Com o [Depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depure JavaScript em execução Microsoft Edge diretamente do Visual Studio Code.  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="O Depurador para Microsoft Edge Extension no Visual Studio Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   O Depurador para Microsoft Edge Extension no Visual Studio Code  
:::image-end:::  

Para obter mais informações, confira [como depurar][VisualStudioCodeDebuggerEdgeExtension]Microsoft Edge de Visual Studio Code .  

#### <a name="webhint"></a>Dica da web  

A [extensão webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code usa `webhint` para melhorar sua página da Web enquanto você a escreve! Essa extensão é executado e relata diagnósticos em seus arquivos de espaço de trabalho com base na `webhint` análise.  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="O webhint Visual Studio Code extensão analisando um arquivo .tsx no Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   O webhint Visual Studio Code extensão analisando um `.tsx` arquivo no Visual Studio Code  
:::image-end:::  

[Saiba mais sobre a extensão Visual Studio Code webhint][WebhintVisualStudioCodeExtension].  

### <a name="visual-studio-integration"></a>Visual Studio integração  

No Visual Studio 2019 versão 16.2 ou posterior, use o depurador Visual Studio para depurar JavaScript em execução no Microsoft Edge.  [Baixe Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso.  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio com a opção de iniciar seu aplicativo Web em Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2019/12/vs.msft.png":::
   Visual Studio com a opção de iniciar seu aplicativo Web em Microsoft Edge Canary, Dev ou Beta  
:::image-end:::  

[Leia nossa postagem de blog para saber como depurar][MicrosoftVisualStudioBlogDebugJavascript]Microsoft Edge de Visual Studio .  

### <a name="tracking-prevention-console-messages"></a>Acompanhamento de mensagens de console de prevenção  

A prevenção de rastreamento é um recurso exclusivo Microsoft Edge impede que você seja rastreado por um site antes de visitar.  A configuração de prevenção de rastreamento padrão é o modo Balanceado, que bloqueia rastreadores de terceiros e rastreadores mal-intencionados conhecidos para uma experiência que equilibra a privacidade e a compatibilidade da Web.  Para dar mais informações sobre a compatibilidade de sua página da Web quando determinados rastreadores são bloqueados Microsoft Edge, a equipe adicionou mensagens de aviso no **Console** quando um rastreador é bloqueado.  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Mensagens no Console quando o controle de prevenção bloqueia o acesso ao armazenamento de um rastreador" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   Mensagens no **Console quando o controle** de prevenção bloqueia o acesso ao armazenamento de um rastreador  
:::image-end:::  

[Leia mais sobre como controlar a prevenção e o equilíbrio entre privacidade e compatibilidade com a Web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 80 que foram contribuídos para o projeto de Chromium de código aberto.  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a>Suporte para redesclarações de let e class no Console  

O **Console** agora dá suporte a reclarações `let` de e `class` instruções.  A incapacidade de redeclarar era um aborrecimento comum para desenvolvedores da Web que usam o Console para experimentar com o novo código JavaScript.  

> [!WARNING]
> Redeclar uma instrução ou em um script fora do Console ou dentro de uma `let` única entrada do Console ainda causa um `class` `SyntaxError` .  

Por exemplo, anteriormente, ao declarar uma variável local com `let` , o Console lançou um erro:  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="O Console no Microsoft Edge 79 mostrando que a redeclaração permitir falha" lightbox="../../images/2019/12/letbefore.msft.png":::
   O **Console** no Microsoft Edge 79 mostrando que a declaração let re-declaration falha  
:::image-end:::  

Agora, o Console permite a reclaração:  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="O Console em Microsoft Edge 80 mostrando que a redeclaração permitir é bem-sucedida" lightbox="../../images/2019/12/letafter.msft.png":::
   O **Console** em Microsoft Edge 80 mostrando que a declaração let re-succeeds  
:::image-end:::  

Chromium problema [#1004193][CR1004193]  

### <a name="improved-webassembly-debugging"></a>Depuração webAssembly aprimorada  

O DevTools começou a dar suporte ao PADRÃO DE Depuração DO ANÃO, o que significa maior suporte para passar por cima do código, definir pontos de interrupção e resolver rastreamentos de pilha em seus idiomas de origem no DevTools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a>Atualizações do painel de rede  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a>Solicitar cadeias de iniciadores no painel Iniciador  

Agora você pode exibir os iniciadores e dependências de uma solicitação de rede como uma lista aninhada.  Isso pode ajudá-lo a entender por que um recurso foi solicitado ou qual atividade de rede um determinado recurso \(como um script\) causou.  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Uma cadeia de iniciador de solicitação no painel Iniciador" lightbox="../../images/2019/12/initiators.msft.png":::
   Uma cadeia de iniciador de solicitação no painel **Iniciador**  
:::image-end:::  

Depois [de registrar atividade de rede][DevToolsNetworkIndex]no painel Rede, escolha um recurso e navegue até o painel **Iniciador** para exibir a **Cadeia de Iniciador de Solicitação**:  

*   O **recurso inspecionado** é negrito.  Na captura de tela acima, `ai.2.min.js` está o recurso inspecionado.  
*   Os recursos acima do recurso inspecionado são os **iniciadores**.  Na captura de tela acima, `https://www.microsoftedgeinsider.com` é o iniciador de `ai.2.min.js` .  Em outras palavras, `https://www.microsoftedgeinsider.com` causou a solicitação de rede para `ai.2.min.js` .  
*   Os recursos abaixo do recurso inspecionado são **as dependências**.  Na captura de tela acima, `https://dc.services.visualstudio.com/v2/track` há uma dependência de `ai.2.min.js` .  Em outras palavras, `ai.2.min.js` causou a solicitação de rede para `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> As informações de inicializador e dependência também podem ser acessadas segurando `Shift` e, em seguida, pairando sobre os recursos de rede.  Navegue [até Exibir iniciadores e dependências.][DevToolsNetworkReferenceDisplayInitiatorsDependencies]  

Chromium problema [#842488][CR842488]  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a>Realça a solicitação de rede selecionada na Visão Geral  

Depois de escolher um recurso de rede para inspecioná-lo, o painel Rede agora coloca uma borda azul ao redor desse recurso na Visão **Geral**.  Isso pode ajudá-lo a detectar se a solicitação de rede está ocorrendo antes ou mais tarde do que o esperado.  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="O painel Visão Geral realçando o recurso inspecionado" lightbox="../../images/2019/12/overview.msft.png":::
   O **painel Visão** Geral realçando o recurso inspecionado  
:::image-end:::  

Chromium problema [#988253][CR988253]  

#### <a name="url-and-path-columns-in-the-network-panel"></a>Colunas de URL e caminho no painel Rede  

Use as novas **colunas Path** e **URL** na ferramenta **Rede** para exibir o caminho absoluto ou a URL completa de cada recurso de rede.  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="As novas colunas Caminho e URL no painel Rede" lightbox="../../images/2019/12/columns.msft.png":::
   As novas colunas Caminho e URL na **ferramenta Rede**  
:::image-end:::  

Para exibir as novas colunas, passe o mouse no header da tabela **Cascata,** abra o menu contextual \(righ-click\) e escolha **Caminho** ou **URL**.  

Chromium problema [#993366][CR993366]  

#### <a name="updated-user-agent-strings"></a>Cadeias User-Agent cadeias de caracteres atualizadas  

O DevTools dá suporte à configuração de uma cadeia User-Agent de caracteres personalizada por meio do **painel Condições de** Rede.  A User-Agent de caracteres afeta o cabeçalho HTTP anexado aos recursos de rede e também `User-Agent` o valor de `navigator.userAgent` .  

As cadeias de caracteres User-Agent foram atualizadas para refletir versões modernas do navegador.  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="O menu Agente do Usuário no painel Condições de Rede" lightbox="../../images/2019/12/useragent.msft.png":::
   O menu Agente do Usuário no painel **Condições de** Rede  
:::image-end:::  

Para acessar **As Condições de Rede,** [abra o Menu de Comando][DevToolsCommandMenuIndex] e execute o `Show Network Conditions` comando.  

> [!NOTE]
> Você também pode [definir User-Agent cadeias de caracteres no Modo de Dispositivo][DevToolsDeviceModeIndex].  

Chromium problema [#1029031][CR1029031]  

### <a name="audits-panel-updates"></a>Atualizações do painel de auditorias  

#### <a name="new-configuration-ui"></a>Nova interface do usuário de configuração  

A interface do usuário de configuração tem um design novo e responsivo e as opções de configuração de otimização foram simplificadas.  Para obter mais informações sobre as alterações na interface do usuário de throttling, navegue até [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="A nova interface do usuário de configuração" lightbox="../../images/2019/12/start.msft.png":::
   A nova interface do usuário de configuração  
:::image-end:::  

### <a name="coverage-tool-updates"></a>Atualizações da ferramenta de cobertura  

#### <a name="per-function-or-per-block-coverage-modes"></a>Modos de cobertura por função ou por bloco  

A [ferramenta Coverage][DevToolsCoverageIndex] tem um novo menu suspenso que permite especificar se os dados de cobertura de código devem ser coletados por **função** ou **por bloco.**  **A cobertura por** bloco é mais detalhada, mas também muito mais cara a ser cobrada.  O DevTools usa **por** padrão a cobertura por função.  

> [!CAUTION]
> Você pode notar grandes diferenças de cobertura de código em arquivos HTML, dependendo se você usa **por função** ou por **modo de** bloqueio.  Ao usar **por modo de** função, scripts em linha em arquivos HTML são tratados como funções.  Se o script for executado, o DevTools marcará todo o script como código usado.  Somente se o script não for executado, o DevTools marcará o script como código nãoutilizado.  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="O menu suspenso do modo de cobertura" lightbox="../../images/2019/12/modes.msft.png":::
   O menu suspenso do modo de cobertura  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a>A cobertura agora deve ser iniciada por uma atualização de página  

A cobertura de código de agregação sem uma atualização de página foi removida porque os dados de cobertura não eram confiáveis.  Por exemplo, uma função pode ser relatada como não usada se o tempo de execução foi há muito tempo e o coletor de lixo V8 a limpou.  

Chromium problema [#1004203][CR1004203]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Encontre código JavaScript e CSS não Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular um modo de exibição móvel - Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkIndex]: ../../../network/index.md "Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Exibir iniciadores e dependências - Referência de Análise de Rede | Microsoft Docs"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Adicione o campo Iniciador à guia Headers | Chromium Bugs"  
[CR988253]: https://crbug.com/988253 "Bug DevTools - Nenhuma associação entre a solicitação de rede e a linha do tempo Graph | Chromium Bugs"  
[CR993366]: https://crbug.com/993366 "Mostre parte do caminho da URL na lista de solicitações do painel de rede | Chromium Bugs"  
[CR1004193]: https://crbug.com/1004193 "Modo REPL para V8 | Chromium Bugs"  
[CR1004203]: https://crbug.com/1004203 "Tornar a Cobertura de Código incrível | Chromium Bugs"  
[CR1029031]: https://crbug.com/1029031 "Cadeias de caracteres da UA estão ficando desatualizadas | Chromium Bugs" 
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Chromium Bugs"
[CR941561]: https://crbug.com/941561 "Localizabilidade do devTools | Chromium Bugs"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Percepções de acessibilidade"  

[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Throttling do Painel de Auditorias do DevTools - GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema - MicrosoftDocs/desenvolvedor de borda"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Canais de visualização"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Depurar JavaScript em Microsoft Edge de Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixar Visual Studio 2019 para Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objeto de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "conta @EdgeDevTools do Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentação webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Code Extension | documentação webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento Microsoft Edge postagem no blog"
[TheWebWeWant]: https://aka.ms/webwewant "A Web Que Queremos"

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developer.chrome.com/blog/new-in-devtools-80) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
