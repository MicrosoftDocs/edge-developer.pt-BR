---
title: O que há de novo no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 10696a49a833475d59a6be1189362fdb0c26a96d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991154"
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

# O que há de novo no DevTools (Microsoft Edge 81)  

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
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

O DevTools corresponde automaticamente ao idioma usado para o Microsoft Edge `edge://settings/languages` .  

Se quiser que o Microsoft Edge esteja em um idioma e seu DevTools permaneça em inglês, pressione `F1` na devtools para abrir [as configurações][Settings] e desabilitar o **idioma do navegador correspondente**.  

> ##### Figura 2  
> O DevTools em alemão  
> ![O DevTools em alemão][ImageLocalizedGerman]  

As mensagens do **console** não são localizadas.  Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma usado para o Microsoft Edge.  

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

Para acessar o modo de exibição 3D, pressione `Ctrl`  +  `Shift`  +  `P` , digite o **modo de exibição 3D** e selecione **Mostrar modo de exibição 3D**.  

Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao modo de exibição 3D, portanto, envie-nos seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).  

Chromium problema [#987787][crbug987787]  

### Extensões de código do Visual Studio  

A equipe do DevTools também lançou algumas extensões para o [código do Visual Studio \ (vs Code \)][VisualStudioCode] que permitem que você use o poder do devtools diretamente do seu editor de texto! Confira as extensões abaixo:  

#### Elementos do Microsoft Edge  

Use a ferramenta de elementos de dentro do código VS adicionando os [elementos para Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs extensão de código.  

> ##### Figura 5  
> A ferramenta elementos em código VS usando os elementos da extensão do Microsoft Edge ![ a ferramenta elementos em vs Code usando os elementos da extensão do Microsoft Edge][ImageElementsVisualStudioCode]  

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

[Saiba mais sobre como depurar o Microsoft Edge do Visual Studio][MicrosoftVisualStudio].  

### Rastrear mensagens do console de prevenção  

A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você contra acompanhamento de sites que ainda não visitou.  A configuração de prevenção de rastreamento padrão é o modo balanceado, que bloqueia os rastreadores de terceiros e os rastreadores mal-intencionados conhecidos para obter uma experiência que equilibre a compatibilidade com a privacidade e a compatibilidade com a Web.  Para fornecer a você mais informações sobre a compatibilidade de sua página da Web quando determinados rastreadores estão bloqueados, também adicionamos mensagens de aviso no console quando um controlador é bloqueado.  

> ##### Figura 9  
> Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador  
> ![Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador][ImageTrackingPrevention]  

[Leia mais sobre a prevenção de rastreamento e o equilíbrio entre a compatibilidade entre privacidade e Web][TrackingPrevention].  

## Anúncios do projeto Chromium  

As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 81 que contribuíram para o projeto de código-fonte aberto Chromium.  

### Suporte do moto G4 no modo de dispositivo  

Depois de [habilitar a barra de ferramentas do dispositivo][DeviceToolbar], simule as dimensões de um visor moto G4 da lista de **dispositivos** .  

> ##### Figura 10  
> Simulando um visor moto G4  
> ![Simulando um visor moto G4][ImageMotoG4]  

Clique em [Mostrar quadro de dispositivo][DeviceFrame] para mostrar o hardware moto G4 em torno do visor.  

> ##### Figura 11  
> Mostrando o hardware moto G4  
> ![Mostrando o hardware moto G4][ImageMotoG4Frame]  

Recursos relacionados:  

*   Abra o [menu de comando][CommandMenu] e execute o `Capture screenshot` comando para fazer uma captura de tela do visor que inclua o hardware moto G4 (após habilitar a **exibição do quadro de dispositivo**).  
*   [Acelera a rede e a CPU][ThrottleNetworkAndCpu] para simular com mais precisão as condições de navegação de um usuário móvel.  

Chromium problema [#924693][crbug924693]  

### Atualizações relacionadas a cookies  

#### Cookies bloqueados no painel cookies  

O painel cookies no painel de aplicativos agora exibe cookies bloqueados com um plano de fundo amarelo.  

> ##### Figura 12  
> Cookies bloqueados no painel cookies do painel do aplicativo  
> ![Cookies bloqueados no painel cookies do painel do aplicativo][ImageBlockedCookies]  

Chromium problema [#1030258][crbug|::ref1::|]  

#### Prioridade do cookie no painel cookies  

As tabelas de cookies nos painéis rede e aplicativo agora incluem uma coluna de **prioridade** .  

> [!CAUTION]
> Navegadores baseados em Chromium, como o Microsoft Edge, são os únicos navegadores que dão suporte à prioridade de cookies.  

Chromium problema [#1026879][crbug1026879]  

#### Editar todos os valores de cookies  

Todas as células nas tabelas de cookies são editáveis agora, exceto as células na coluna **tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.  Veja os [campos][CookiesFields] para obter uma explicação de cada coluna.  

> ##### Figura 13  
> Editando um valor de cookie  
> ![Editando um valor de cookie][ImageEditCookie]  

#### Copiar como Node.js FETCH para incluir dados de cookies  

Clique com o botão direito do mouse em uma solicitação de rede e selecione **copiar**  >  **cópia como Node.js FETCH** para obter uma `fetch` expressão que inclua dados de cookies.  

> ##### Figura 14  
> Copiar como Node.js Fetch  
> ![Copiar como Node.js Fetch][ImageCopyFetch]  

Chromium problema [#1029826][crbug1029826]  

### Ícones mais precisos de manifesto do aplicativo Web  

Anteriormente, o painel de manifesto no painel do aplicativo enviou suas próprias solicitações para exibir os ícones de manifesto do aplicativo Web.  O DevTools agora mostra o mesmo ícone de manifesto usado pelo Microsoft Edge.  

> ##### Figura 15  
> Ícones no painel manifestar  
> ![Ícones no painel manifestar][ImageManifestIcon]  

Chromium problema [#985402][crbug985402]  

### Passe o mouse sobre as propriedades do conteúdo CSS para ver os valores sem escape  

Passe o mouse sobre o valor de uma `content` propriedade para ver a versão sem escape do valor.  

Por exemplo, nesta [demonstração][CSSContentDemo] ao inspecionar o `p::after` pseudo elemento, você vê uma cadeia de caracteres de escape no painel estilos:  

> ##### Figura 16  
> A cadeia de caracteres de escape  
> ![A cadeia de caracteres de escape][ImageEscapedString]  

Ao passar o mouse sobre o `content` valor, você vê o valor indesejado:  

> ##### Figura 17  
> O valor não-escape  
> ![O valor não-escape][ImageUnescapedString]  

### Erros de mapa de origem mais detalhados no console  

Agora, o console fornece mais detalhes sobre o motivo pelo qual um mapa de origem falhou ao carregar ou analisar.  Anteriormente, era fornecido um erro sem explicar o que aconteceu de errado.  

> ##### Figura 18  
> Um erro de carregamento do mapa de origem no console  
> ![Um erro de carregamento do mapa de origem no console][ImageSourcemapError]  

### Configuração para desativar a rolagem após o final de um arquivo  

Abra [configurações][Settings] e, em **Preferences**seguida, desabilite as  >  **fontes**  >  **de preferências permitem a rolagem do final do arquivo** para desativar o comportamento padrão da interface do usuário que permite rolar bem após o final de um arquivo no painel **fontes** .  

> ##### Figura 19  
> Desativando **permitir rolagem após o fim do arquivo** em configurações  
> ![Desativando permitir rolagem após o final do arquivo][ImageSettings]  

> ##### Figura 20  
> A rolagem após o final de um arquivo agora está desabilitada no painel fontes  
> ![A rolagem após o final de um arquivo agora está desabilitada no painel fontes][ImageScroll]  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge DevTools equipe  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Figura 1: a ferramenta de desempenho no DevTools com as melhorias de navegação do teclado e do leitor de tela"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Figura 2: o DevTools em alemão"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Figura 3: a guia dicas no Microsoft Edge DevTools quando a extensão do navegador webhints está instalada"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Figura 4: modo de exibição 3D no Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Figura 5: a ferramenta elementos no código VS usando os elementos da extensão do Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Figura 6: o depurador para extensão do Microsoft Edge no código VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Figura 7: a extensão de código do webhint x que analisa arquivos. TSX no código VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Figura 8: Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Figura 9: mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Figura 10: simulando um visor moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Figura 11: mostrando o hardware moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Figura 12: cookies bloqueados no painel cookies do painel do aplicativo"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Figura 13: editando um valor de cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Figura 14: copiar como Node.js Fetch"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Figura 15: ícones no painel de manifesto"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Figura 16: a cadeia de caracteres de escape"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Figura 17: o valor não-escape"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Figura 18: um erro de carregamento do mapa de origem no console"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Figura 19: desativando permitir rolagem após o fim do arquivo em configurações"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Figura 20: rolar após o final de um arquivo agora está desabilitado no painel fontes"

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular um visor móvel com o modo de dispositivo no Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Selecione Mostrar quadro de dispositivo para mostrar a estrutura do dispositivo físico em torno do visor."
[CommandMenu]: ../../../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limite a rede e a CPU para simular com mais precisão as condições de navegação de um usuário móvel."
[crbug924693]: https://crbug.com/924693 "924693: solicitação de recurso: Adicionar moto G4 à lista de modo de dispositivo"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: a guia cookies no console de desenvolvimento não mostra mais prioridade"
[CookiesFields]: ../../../storage/cookies.md#fields "Os campos na tabela de cookies"
[crbug1029826]: https://crbug.com/1029826 "1029826: guia rede-> clique com o botão direito do mouse para solicitar-> copiar-> copiar como busca não copiar cookies"
[crbug985402]: https://crbug.com/985402 "985402: o erro do ícone do manifesto do aplicativo Web cadeia de caracteres de erro é confuso"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração de conteúdo CSS não escape"
[Settings]: ../../../customize/index.md#settings "Personalizar o Microsoft Edge DevTools com configurações"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para extensão de código do Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos da extensão de código do Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools não são compatíveis com a WCAG"
[crbug941561]: https://crbug.com/941561 "941561-localização da DevTools"
[crbug987787]: https://crbug.com/987787 "987787-modo de exibição 3D dom"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Informações sobre acessibilidade"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos do Microsoft Edge Insider"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixe o Visual Studio 2019 para Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (modelo de objeto de documento) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-índice | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Código do Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \ (Chromium \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensão do navegador webhint | documentação do webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint VS extensão de código | documentação do webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem de blog do Microsoft Edge"

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/01/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  