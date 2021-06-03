---
description: Exibição 3D, Visual Studio integração com Microsoft Edge e muito mais.
title: Novidades no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 03b17f524e9be55e1ed37147ce46b7a15fc3a17d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564956"
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
# <a name="whats-new-in-devtools-microsoft-edge-81"></a>Novidades no DevTools (Microsoft Edge 81)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Comunicados da equipe Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe Microsoft Edge DevTools.  Confira os comunicados para experimentar novos recursos no DevTools, Microsoft Visual Studio Extensões de Código e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais Microsoft Edge [de][MicrosoftEdgePreviewChannels] visualização e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### <a name="accessibility-improvements-to-the-devtools"></a>Melhorias de acessibilidade no DevTools  

A equipe do DevTools contribuiu com 170 alterações no Chromium para resolver problemas de contraste de cores de alto impacto, teclado e leitor de tela no DevTools.  Cada desenvolvedor que está criando a Web deve ser capaz de usar o DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="A ferramenta Performance no DevTools com as melhorias de navegação de teclado e leitor de tela" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
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
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

O DevTools corresponderá automaticamente ao idioma usado para Microsoft Edge em `edge://settings/languages` .  

Se você quiser Microsoft Edge em um idioma e seu DevTools permanecer em inglês, selecione no DevTools para abrir Configurações e desabilitar o idioma do navegador `F1` **match.** [][DevtoolsCustomizeIndexSettings]  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   O DevTools em alemão  
:::image-end:::  

**As mensagens** de console não são localizadas.  Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma usado para Microsoft Edge.  

Se você quiser usar o DevTools em um idioma diferente dos que estão disponíveis, [tweet][PostTweetEdgeDevTools] para nós ou escolha o [ícone Enviar Comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium problema [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>webhint Microsoft Edge extensão  

A extensão webhint Microsoft Edge permite que você digitalizar facilmente sua página da Web e obter comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.  Leia mais em [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="A ferramenta Hints no DevTools quando a extensão do navegador webhint é instalada" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   A **ferramenta Hints** no DevTools quando a extensão do navegador webhint é instalada  
:::image-end:::  

[Experimente a extensão do navegador webhint em Microsoft Edge][MicrosoftEdgeInsiderAddons].  Depois de instalar a extensão, abra o DevTools e escolha a **ferramenta Dicas.**  A partir daqui, execute uma verificação de site personalizável.  Vá até [webhint.io][WebhintBrowserExtension] para saber mais.  

### <a name="3d-view"></a>Modo de exibição 3D  

Use o **View 3D** para depurar seu aplicativo Web navegando pelo modelo de objeto de documento [\(DOM\)][MDNDocumentObjectModel] ou o contexto de empilhamento [de índice z.][MDNZIndex]  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="A exibição 3D no DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   A exibição 3D no DevTools  
:::image-end:::  

Para acessar o View 3D, selecione `Ctrl`  +  `Shift`  +  `P` , digite No **3D View** e selecione **Mostrar Exibição 3D**.  

A Microsoft Edge equipe está trabalhando com a equipe Chromium na interface do usuário e adicionando mais funcionalidade ao Modo de Exibição 3D, portanto, envie seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).  

Chromium problema [#987787][CR987787]  

### <a name="visual-studio-code-extensions"></a>Visual Studio Code extensões  

A equipe do DevTools também [][VisualStudioCode] lançou algumas extensões para Visual Studio Code que permitem que você use o poder do DevTools diretamente do editor de texto! Confira as extensões abaixo:  

#### <a name="elements-for-microsoft-edge"></a>Elementos para Microsoft Edge  

Use a ferramenta Elements de dentro Visual Studio Code adicionando a extensão [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="A ferramenta Elements no Visual Studio Code usando os elementos para Microsoft Edge extensão" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   A **ferramenta Elements** no Visual Studio Code usando os elementos para Microsoft Edge extensão  
:::image-end:::  

Para obter mais informações, confira [Elementos para Microsoft Edge Visual Studio Code extensão][VisualStudioCodeElementEdgeExtension].  

#### <a name="debugger-for-microsoft-edge"></a>Depurador para Microsoft Edge  

Com o [Depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depure JavaScript em execução Microsoft Edge diretamente do Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="O Depurador para Microsoft Edge Extension no Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   O Depurador para Microsoft Edge Extension no Visual Studio Code  
:::image-end:::  

Para obter mais informações, confira [como depurar][VisualStudioCodeDebuggerEdgeExtension]Microsoft Edge de Visual Studio Code .  

#### <a name="webhint"></a>Dica da web  

A [extensão webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code usa `webhint` para melhorar sua página da Web enquanto você a escreve.  Essa extensão é executado e relata diagnósticos em seus arquivos de espaço de trabalho com base na `webhint` análise.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="O webhint Visual Studio Code extensão analisando um arquivo .tsx no Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   O webhint Visual Studio Code extensão analisando um `.tsx` arquivo no Visual Studio Code  
:::image-end:::  

[Saiba mais sobre a extensão Visual Studio Code webhint][WebhintVisualStudioCodeExtension].  

### <a name="visual-studio-integration"></a>Visual Studio integração  

No Visual Studio 2019 versão 16.2 ou posterior, use o depurador Visual Studio para depurar JavaScript em execução no Microsoft Edge.  [Baixe Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso!  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio com a opção de iniciar seu aplicativo Web em Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio com a opção de iniciar seu aplicativo Web em Microsoft Edge Canary, Dev ou Beta  
:::image-end:::  

[Saiba mais sobre a depuração Microsoft Edge de Visual Studio][VisualStudioIndex].  

### <a name="tracking-prevention-console-messages"></a>Acompanhamento de mensagens de console de prevenção  

A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você de ser rastreado por sites que você não visitou antes.  A configuração de prevenção de rastreamento padrão é o modo Balanceado, que bloqueia rastreadores de terceiros e rastreadores mal-intencionados conhecidos para uma experiência que equilibra a privacidade e a compatibilidade da Web.  Para dar mais informações sobre a compatibilidade da página da Web quando determinados rastreadores são bloqueados, as mensagens de aviso foram adicionadas ao **Console** quando um rastreador é bloqueado.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensagens no Console quando o controle de prevenção bloqueia o acesso ao armazenamento de um rastreador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Mensagens no **Console quando o controle** de prevenção bloqueia o acesso ao armazenamento de um rastreador  
:::image-end:::  

[Leia mais sobre como controlar a prevenção e o equilíbrio entre privacidade e compatibilidade com a Web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 81 que foram contribuídos para o projeto de Chromium de código aberto.  

### <a name="moto-g4-support-in-device-mode"></a>Suporte ao Moto G4 no Modo de Dispositivo  

Depois [de habiltar][DevtoolsDeviceModeIndexSimulateMobileViewport]a Barra de Ferramentas de Dispositivo, simule as dimensões de um viewport do Moto G4 na **lista Dispositivo.**  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulando um viewport do Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Simulando um viewport do Moto G4  
:::image-end:::  

Escolha [Mostrar Quadro de Dispositivo][DevtoolsDeviceModeIndexShowDeviceFrame] para mostrar o hardware do Moto G4 ao redor do viewport.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrando o hardware do Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Mostrando o hardware do Moto G4  
:::image-end:::  

Recursos relacionados:  

*   Abra o [Menu de Comando][DevtoolsCommandMenuIndex] e execute o comando para fazer uma captura de tela do viewport que inclui o hardware do Moto G4 (depois de habiltar `Capture screenshot` **Show Device Frame**).  
*   [Acelere a rede e a CPU][DevtoolsDeviceModeIndexThrottleNetworkCpu] para simular com mais precisão as condições de navegação da Web de um usuário móvel.  

Chromium problema [#924693][CR924693]  

### <a name="cookie-related-updates"></a>Atualizações relacionadas a cookies  

#### <a name="blocked-cookies-in-the-cookies-pane"></a>Cookies bloqueados no painel Cookies  

O painel Cookies no painel Aplicativo agora exibe cookies bloqueados com um plano de fundo amarelo.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueados no painel Cookies do painel Aplicativo" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Cookies bloqueados no painel Cookies do painel Aplicativo  
:::image-end:::  

Chromium problema [#1030258][CR1030258]  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a>Prioridade de cookie no painel Cookie  

As tabelas Cookies nas **ferramentas Rede** **e Aplicativo** agora incluem uma **coluna Priority.**  

> [!CAUTION]
> Chromium navegadores baseados em cookies, como Microsoft Edge, são os únicos navegadores que suportam prioridade de cookie.  

Chromium problema [#1026879][CR1026879]  

#### <a name="edit-all-cookie-values"></a>Editar todos os valores de cookie  

Todas as células nas tabelas Cookie agora podem ser editadas, exceto células na coluna **Tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.  Para uma explicação de cada coluna, navegue até [Campos][DevtoolsStorageCookiesFields].  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Editar um valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Editar um valor de cookie  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a>Copiar como Node.js buscar para incluir dados de cookie  

Para obter uma expressão que inclua dados de cookie, passe o mouse em uma solicitação de rede, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar Cópia como Node.js `fetch` ****  >  **buscar**.  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js busca" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Copiar como Node.js busca  
:::image-end:::  

Chromium problema [#1029826][CR1029826]  

### <a name="more-accurate-web-app-manifest-icons"></a>Ícones de manifesto de aplicativo web mais precisos  

Anteriormente, o painel Manifesto no painel Aplicativo enviava suas próprias solicitações para exibir ícones de manifesto do aplicativo Web.  O DevTools agora mostra o mesmo ícone de manifesto que Microsoft Edge usa.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Ícones no painel Manifesto" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Ícones no painel Manifesto  
:::image-end:::  

Chromium problema [#985402][CR985402]  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a>Passe o mouse em propriedades de conteúdo CSS para exibir valores não-escapados  

Passe o mouse no valor de uma propriedade para exibir a versão não `content` paisagem do valor.  

Por exemplo, nesta [demonstração][CSSContentDemo] quando você inspeciona o pseudo-elemento, uma cadeia de caracteres de escape `p::after` é exibida no painel **Estilos:**  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="A cadeia de caracteres de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   A cadeia de caracteres de escape  
:::image-end:::  

Quando você passar o mouse sobre `content` o valor, o valor não escapou é exibido.  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="O valor não-escapado" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   O valor não-escapado  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a>Erros de mapa de origem mais detalhados no Console  

O Console agora fornece mais detalhes sobre por que um mapa de origem falhou ao carregar ou analisar.  Anteriormente, ele apenas forneceu um erro sem explicar o que deu errado.  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Um erro de carregamento de mapa de origem no Console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   Um erro de carregamento de mapa de origem no Console  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a>Configuração para desabilitar a rolagem após o final de um arquivo  

Abra [Configurações][DevtoolsCustomizeIndexSettings] e desabilite Fontes de **Preferências**Permitir rolagem no final do arquivo para desabilitar o comportamento padrão da interface do usuário que permite que você role bem além do final de um arquivo no painel  >  ****  >  **** **Fontes.**  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Desabilitar Permitir a rolagem do final passado do arquivo" lightbox="../../images/2020/01/settings.msft.png":::
   Desabilitar **Permitir a rolagem do final do arquivo no** Configurações  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="A rolagem além do final de um arquivo agora está desabilitada no painel Fontes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   A rolagem além do final de um arquivo agora está desabilitada no painel Fontes  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular um modo de exibição móvel - Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsDeviceModeIndexShowDeviceFrame]: ../../../device-mode/index.md#show-device-frame "Mostrar quadro do dispositivo - Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexThrottleNetworkCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Acelerar a rede e a CPU - Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsStorageCookiesFields]: ../../../storage/cookies.md#fields "Campos - Exibir, editar e excluir cookies com Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioIndex]: ../../../../visual-studio/index.md "Visual Studio | Microsoft Docs"  

[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos para Microsoft Edge \(Chromium\) | Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"

[TrackingPrevention]: https://blogs.windows.com/msedgedev/2019/12/03/improving-tracking-prevention-microsoft-edge-79 "Melhorando a prevenção de rastreamento Microsoft Edge postagem no blog"

[MicrosoftEdgeInsiderAddons]: https://microsoftedge.microsoft.com/addons/detail/webhint/mlgfbihcfnkaenjpdcngdnhcpkdmcdee "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Baixar Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um Tweet"  

[CR924693]: https://crbug.com/924693 "Solicitação de Recurso: Adicionar o Moto G4 à lista de | Chromium Bugs"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Chromium Bugs"  
[CR1026879]: https://crbug.com/1026879 "A guia Cookie no console de dev não mostra mais a prioridade | Chromium Bugs"  
[CR1029826]: https://crbug.com/1029826 "guia de rede -> escolha solicitar -> cópia -> cópia como busca não copia cookies | Chromium Bugs"  
[CR985402]: https://crbug.com/985402 "Cadeias de erro de ícone de manifesto do aplicativo web são confusas | Chromium Bugs"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Chromium Bugs"  
[CR941561]: https://crbug.com/941561 "Localizabilidade do devTools | Chromium Bugs"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração para conteúdo CSS sem paisagem"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

[TheWebWeWant]: https://webwewant.fyi "A Web que queremos"  
[AccessibilityInsights]: https://accessibilityinsights.io "Percepções de acessibilidade"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objeto de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "conta @EdgeDevTools do Twitter"  

[Webhint]: https://webhint.io "webhint"  

[WebhintBrowserExtension]: https://webhint.io/docs/user-guide/extensions/extension-browser "Webhint Browser Extension | documentação webhint"  
[WebhintVisualStudioCodeExtension]: https://webhint.io/docs/user-guide/extensions/vscode-webhint "Webhint Visual Studio Code Extension | documentação webhint"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developer.chrome.com/blog/new-in-devtools-81) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  