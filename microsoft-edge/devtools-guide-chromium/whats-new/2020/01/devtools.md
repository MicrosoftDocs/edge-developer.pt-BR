---
description: Exibição 3D, Visual Studio integração com o Microsoft Edge e muito mais.
title: Novidades no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ddd48b78c59e26edc9bca159f5ddf684015ae980
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514407"
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

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Comunicados da equipe do Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.  Confira os comunicados para experimentar novos recursos no DevTools, no Microsoft Visual Studio Code e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### <a name="accessibility-improvements-to-the-devtools"></a>Melhorias de acessibilidade no DevTools  

A equipe do DevTools contribuiu com 170 alterações no Chromium para resolver problemas de contraste de cores de alto impacto, teclado e leitor de tela no DevTools.  Cada desenvolvedor que está criando a Web deve ser capaz de usar o DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="A ferramenta Performance no DevTools com as melhorias de navegação de teclado e leitor de tela" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   A **ferramenta Performance** no DevTools com as melhorias de navegação de teclado e leitor de tela  
:::image-end:::  

Quer saber como tornar sua página da Web acessível para todos os usuários?  Baixe as [Percepções de Acessibilidade][AccessibilityInsights] [e extensões webhint][WebhintBrowserExtension] do Microsoft Edge para começar.  

Se você usar leitores de tela ou o teclado para navegar [][PostTweetEdgeDevTools] ao redor do DevTools, envie seus comentários tuitando para nós ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#963183][CR963183]  

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

O DevTools corresponderá automaticamente ao idioma que você usa para o Microsoft Edge em `edge://settings/languages` .  

Se você quiser que o Microsoft Edge fique em um idioma e seu DevTools permaneça em inglês, selecione no DevTools para abrir Configurações e desabilitar Corresponder idioma `F1` **do navegador**. [][Settings]  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   O DevTools em alemão  
:::image-end:::  

**As mensagens** de console não são localizadas.  Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma que você usa para o Microsoft Edge.  

Se você quiser usar o DevTools em um idioma diferente dos que estão disponíveis, [tweet][PostTweetEdgeDevTools] para nós ou escolha o [ícone Enviar Comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>extensão webhint do Microsoft Edge  

A extensão webhint do Microsoft Edge permite que você digitalizar facilmente sua página da Web e obter comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.  Leia mais em [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="A ferramenta Hints no DevTools quando a extensão do navegador webhint é instalada" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   A **ferramenta Hints** no DevTools quando a extensão do navegador webhint é instalada  
:::image-end:::  

[Experimente a extensão do navegador webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].  Depois de instalar a extensão, abra o DevTools e escolha a **ferramenta Dicas.**  A partir daqui, execute uma verificação de site personalizável.  Vá até [webhint.io][WebhintBrowserExtension] para saber mais.  

### <a name="3d-view"></a>Modo de exibição 3D  

Use o **View 3D** para depurar seu aplicativo Web navegando pelo modelo de objeto de documento [\(DOM\)][MDNDocumentObjectModel] ou o contexto de empilhamento [de índice z.][MDNZIndex]  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="A exibição 3D no DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   A exibição 3D no DevTools  
:::image-end:::  

Para acessar o View 3D, selecione `Ctrl`  +  `Shift`  +  `P` , digite No **3D View** e selecione **Mostrar Exibição 3D**.  

A equipe do Microsoft Edge está trabalhando com a equipe do Chromium na interface do usuário e adicionando mais funcionalidade ao Modo de Exibição 3D, portanto, envie seus [comentários.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problema do Chromium [#987787][CR987787]  

### <a name="visual-studio-code-extensions"></a>Visual Studio extensões de código  

A equipe do DevTools também lançou algumas extensões para Visual Studio [Code][VisualStudioCode] que permitem que você use o poder do DevTools diretamente do seu editor de texto! Confira as extensões abaixo:  

#### <a name="elements-for-microsoft-edge"></a>Elementos para o Microsoft Edge  

Use a ferramenta Elements de dentro Visual Studio Code adicionando a extensão [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="A ferramenta Elements no Visual Studio Code usando a extensão Elements for Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   A **ferramenta Elements** no Visual Studio Code usando a extensão Elements for Microsoft Edge  
:::image-end:::  

Para obter mais informações, confira [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].  

#### <a name="debugger-for-microsoft-edge"></a>Depurador para o Microsoft Edge  

Com a [extensão Depurador do Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depure JavaScript em execução no Microsoft Edge diretamente do Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="O Depurador para a Extensão do Microsoft Edge em Visual Studio Código" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   O Depurador para a Extensão do Microsoft Edge em Visual Studio Código  
:::image-end:::  

Para obter mais informações, confira [como depurar o Microsoft Edge de Visual Studio Código][VisualStudioCodeDebuggerEdgeExtension].  

#### <a name="webhint"></a>Dica da web  

A [extensão webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code usa `webhint` para melhorar sua página da Web enquanto você a escreve.  Essa extensão é executado e relata diagnósticos em seus arquivos de espaço de trabalho com base na `webhint` análise.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="A extensão webhint Visual Studio Code analisando um arquivo .tsx em Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   A extensão webhint Visual Studio Code analisando um `.tsx` arquivo em Visual Studio Code  
:::image-end:::  

[Saiba mais sobre a extensão webhint Visual Studio Code][WebhintVisualStudioCodeExtension].  

### <a name="visual-studio-integration"></a>Visual Studio integração  

No Visual Studio 2019 versão 16.2 ou posterior, use o depurador Visual Studio para depurar JavaScript em execução no Microsoft Edge.  [Baixe Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso!  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canary, Dev ou Beta  
:::image-end:::  

[Saiba mais sobre a depuração do Microsoft Edge Visual Studio][MicrosoftVisualStudio].  

### <a name="tracking-prevention-console-messages"></a>Acompanhamento de mensagens de console de prevenção  

A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você de ser rastreado por sites que você não visitou antes.  A configuração de prevenção de rastreamento padrão é o modo Balanceado, que bloqueia rastreadores de terceiros e rastreadores mal-intencionados conhecidos para uma experiência que equilibra a privacidade e a compatibilidade da Web.  Para dar mais informações sobre a compatibilidade da página da Web quando determinados rastreadores são bloqueados, as mensagens de aviso foram adicionadas ao **Console** quando um rastreador é bloqueado.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensagens no Console quando o controle de prevenção bloqueia o acesso ao armazenamento de um rastreador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Mensagens no **Console quando o controle** de prevenção bloqueia o acesso ao armazenamento de um rastreador  
:::image-end:::  

[Leia mais sobre como controlar a prevenção e o equilíbrio entre privacidade e compatibilidade com a Web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 81 que contribuíram para o projeto Chromium de código aberto.  

### <a name="moto-g4-support-in-device-mode"></a>Suporte ao Moto G4 no Modo de Dispositivo  

Depois [de habiltar][DeviceToolbar]a Barra de Ferramentas de Dispositivo, simule as dimensões de um viewport do Moto G4 na **lista Dispositivo.**  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulando um viewport do Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Simulando um viewport do Moto G4  
:::image-end:::  

Escolha [Mostrar Quadro de Dispositivo][DeviceFrame] para mostrar o hardware do Moto G4 ao redor do viewport.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrando o hardware do Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Mostrando o hardware do Moto G4  
:::image-end:::  

Recursos relacionados:  

*   Abra o [Menu de Comando][CommandMenu] e execute o comando para fazer uma captura de tela do viewport que inclui o hardware do Moto G4 (depois de habiltar `Capture screenshot` **Show Device Frame**).  
*   [Acelere a rede e a CPU][ThrottleNetworkAndCpu] para simular com mais precisão as condições de navegação da Web de um usuário móvel.  

Problema do Chromium [#924693][CR924693]  

### <a name="cookie-related-updates"></a>Atualizações relacionadas a cookies  

#### <a name="blocked-cookies-in-the-cookies-pane"></a>Cookies bloqueados no painel Cookies  

O painel Cookies no painel Aplicativo agora exibe cookies bloqueados com um plano de fundo amarelo.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueados no painel Cookies do painel Aplicativo" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Cookies bloqueados no painel Cookies do painel Aplicativo  
:::image-end:::  

Problema do Chromium [#1030258][CR1030258]  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a>Prioridade de cookie no painel Cookie  

As tabelas Cookies nas **ferramentas Rede** **e Aplicativo** agora incluem uma **coluna Priority.**  

> [!CAUTION]
> Os navegadores baseados em Chromium, como o Microsoft Edge, são os únicos navegadores que suportam prioridade de cookie.  

Problema do Chromium [#1026879][CR1026879]  

#### <a name="edit-all-cookie-values"></a>Editar todos os valores de cookie  

Todas as células nas tabelas Cookie agora podem ser editadas, exceto células na coluna **Tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.  Para uma explicação de cada coluna, navegue até [Campos][CookiesFields].  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Editar um valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Editar um valor de cookie  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a>Copiar como Node.js buscar para incluir dados de cookie  

Para obter uma expressão que inclua dados de cookie, passe o mouse em uma solicitação de rede, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar Cópia como Node.js `fetch` ****  >  **buscar**.  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js busca" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Copiar como Node.js busca  
:::image-end:::  

Problema do Chromium [#1029826][CR1029826]  

### <a name="more-accurate-web-app-manifest-icons"></a>Ícones de manifesto de aplicativo web mais precisos  

Anteriormente, o painel Manifesto no painel Aplicativo enviava suas próprias solicitações para exibir ícones de manifesto do aplicativo Web.  O DevTools agora mostra o mesmo ícone de manifesto que o Microsoft Edge usa.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Ícones no painel Manifesto" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Ícones no painel Manifesto  
:::image-end:::  

Problema do Chromium [#985402][CR985402]  

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

Abra [Configurações][Settings] e desabilite Fontes de **Preferências**Permitir rolagem no final do arquivo para desabilitar o comportamento padrão da interface do usuário que permite que você role bem além do final de um arquivo no painel  >  ****  >  **** **Fontes.**  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Desabilitar Permitir a rolagem do final passado do arquivo" lightbox="../../images/2020/01/settings.msft.png":::
   Desabilitar **Permitir a rolagem do final passado do arquivo** em Configurações  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="A rolagem além do final de um arquivo agora está desabilitada no painel Fontes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   A rolagem além do final de um arquivo agora está desabilitada no painel Fontes  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular um modo de exibição móvel - Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Docs"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Mostrar quadro do dispositivo - Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Docs"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Acelerar a rede e a CPU - Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Docs"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Microsoft Docs"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Campos - Exibir, editar e excluir cookies com o Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para a extensão Visual Studio Código do Microsoft Edge"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos para a extensão Visual Studio Código do Microsoft Edge"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de Visualização do Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Código"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para o Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos do Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem do blog do Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixar Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um Tweet"  

[CR924693]: https://crbug.com/924693 "Solicitação de Recurso: Adicionar o Moto G4 à lista de | Bugs de cromo"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Bugs de cromo"  
[CR1026879]: https://crbug.com/1026879 "A guia Cookie no console de dev não mostra mais a prioridade | Bugs de cromo"  
[CR1029826]: https://crbug.com/1029826 "guia de rede -> escolha solicitar -> cópia -> cópia como busca não copia cookies | Bugs de cromo"  
[CR985402]: https://crbug.com/985402 "Cadeias de erro de ícone de manifesto do aplicativo web são confusas | Bugs de cromo"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Bugs de cromo"  
[CR941561]: https://crbug.com/941561 "Localizabilidade do devTools | Bugs de cromo"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Bugs de cromo"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração para conteúdo CSS sem paisagem"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Percepções de acessibilidade"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objeto de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "conta @EdgeDevTools do Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentação webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Code Extension | documentação webhint"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developer.chrome.com/blog/new-in-devtools-81) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  