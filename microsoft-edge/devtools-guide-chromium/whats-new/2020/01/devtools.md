---
description: Modo de exibição 3D, integração do Visual Studio com o Microsoft Edge e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3081ebb256a9ede637aaaddc3c3cdf7a70a201bb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015472"
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

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools! Dê uma olhada neles para experimentar novos recursos no DevTools, extensões de código do Visual Studio e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### Melhorias de acessibilidade no DevTools  

A equipe do DevTools contribuiu com as mudanças do 170 para o Chromium para solucionar problemas de cor de alto impacto, teclado e leitor de tela no DevTools.  Cada desenvolvedor que cria a Web deve poder usar o DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="A ferramenta desempenho no DevTools com melhorias de navegação do teclado e leitor de tela" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   A ferramenta **desempenho** no devtools com melhorias de navegação do teclado e leitor de tela  
:::image-end:::  

Deseja saber como tornar sua página da Web acessível a todos os seus usuários?  Baixe as [informações sobre acessibilidade][AccessibilityInsights] e as extensões [webhint][WebhintBrowserExtension] para o Microsoft Edge para começar.  

Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !  

Chromium problema [#963183][CR963183]  

### Usando o DevTools em outros idiomas  

Muitos desenvolvedores usam outras ferramentas de desenvolvedor, como o código do StackOverflow e do Visual Studio, em seu idioma nativo, não apenas em inglês.  Estamos entusiasmados a anunciar a localização do DevTools, que agora você pode usar em um dos dez idiomas além do inglês:  

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

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="O DevTools em alemão" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   O DevTools em alemão  
:::image-end:::  

As mensagens do **console** não são localizadas.  Somente as cadeias de caracteres usadas na interface do usuário do DevTools são exibidas no idioma usado para o Microsoft Edge.  

Se você quiser usar o DevTools em um idioma diferente daqueles que estão disponíveis, [tweet][PostTweetEdgeDevTools] conosco ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) .  

Chromium problema [#941561][CR941561]  

### extensão do Microsoft Edge da WebDicas  

A extensão WebDicas da Microsoft Edge permite que você examine facilmente sua página da Web e obtenha comentários sobre acessibilidade, compatibilidade do navegador, segurança, desempenho e muito mais no DevTools.  Leia mais em [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="A guia dicas no DevTools quando a extensão do navegador da WebDicas está instalada" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   A guia **dicas** no devtools quando a extensão do navegador da WebDicas está instalada  
:::image-end:::  

[Experimente a extensão do navegador da webhint no Microsoft Edge][MicrosoftEdgeInsiderAddons].  Depois de instalar a extensão, abra a DevTools e selecione a guia dicas.  Aqui, execute uma verificação de site personalizável.  Vá para [webhint.Io][WebhintBrowserExtension] para saber mais.  

### Modo de exibição 3D  

Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do [modelo de objeto de documento \ (dom \)][MDNDocumentObjectModel] ou do contexto de empilhamento de [índice z][MDNZIndex] .  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="O modo de exibição 3D no DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   O modo de exibição 3D no DevTools  
:::image-end:::  

Para acessar o modo de exibição 3D, pressione `Ctrl`  +  `Shift`  +  `P` , digite o **modo de exibição 3D** e selecione **Mostrar modo de exibição 3D**.  

Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao modo de exibição 3D, portanto, envie-nos seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team).  

Chromium problema [#987787][CR987787]  

### Extensões de código do Visual Studio  

A equipe do DevTools também lançou algumas extensões para o [código do Visual Studio][VisualStudioCode] que permitem usar o poder do devtools diretamente do seu editor de texto! Confira as extensões abaixo:  

#### Elementos do Microsoft Edge  

Use a ferramenta elementos de dentro do código do Visual Studio adicionando os [elementos para o Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] extensão de código do Visual Studio.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="A ferramenta elementos no código do Visual Studio usando os elementos da extensão do Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   A ferramenta **elementos** no código do Visual Studio usando os elementos da extensão do Microsoft Edge  
:::image-end:::  

Para obter mais informações, consulte os [elementos da extensão de código do Microsoft Edge Visual Studio][VisualStudioCodeElementEdgeExtension].  

#### Depurador para Microsoft Edge  

Com o [depurador para extensão de código do Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio, depure o JavaScript executando no Microsoft Edge diretamente do código do Visual Studio.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="O depurador para extensão do Microsoft Edge no código do Visual Studio" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   O depurador para extensão do Microsoft Edge no código do Visual Studio  
:::image-end:::  

Para obter mais informações, confira [como depurar o Microsoft Edge pelo código do Visual Studio][VisualStudioCodeDebuggerEdgeExtension].  

#### Dica da web  

A extensão de código do [webdica][VisualStudioMarketplaceWebhintExtension] Visual Studio usa `webhint` para melhorar sua página da Web enquanto você está escrevendo! Esta extensão executa e relata os diagnósticos nos arquivos do espaço de trabalho com base na `webhint` análise.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="A extensão de código do webdica Visual Studio analisando um arquivo. TSX no código do Visual Studio" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   A extensão de código do webdica Visual Studio analisando um `.tsx` arquivo no código do Visual Studio  
:::image-end:::  

[Saiba mais sobre a extensão webdica de código do Visual Studio][WebhintVisualStudioCodeExtension].  

### Integração do Visual Studio  

No Visual Studio 2019 versão 16,2 ou posterior, use o depurador do Visual Studio para Depurar JavaScript em execução no Microsoft Edge.  [Baixe o Visual Studio 2019][MicrosoftVisualStudioDownloads] para experimentar esse recurso.  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta" lightbox="../../images/2020/01/vs.msft.png":::
   O Visual Studio com a opção de iniciar seu aplicativo Web no Microsoft Edge Canárias, dev ou beta  
:::image-end:::  

[Saiba mais sobre como depurar o Microsoft Edge do Visual Studio][MicrosoftVisualStudio].  

### Rastrear mensagens do console de prevenção  

A prevenção de rastreamento é um recurso exclusivo no Microsoft Edge que protege você contra acompanhamento de sites que ainda não visitou.  A configuração de prevenção de rastreamento padrão é o modo balanceado, que bloqueia os rastreadores de terceiros e os rastreadores mal-intencionados conhecidos para obter uma experiência que equilibre a compatibilidade com a privacidade e a compatibilidade com a Web.  Para fornecer a você mais informações sobre a compatibilidade de sua página da Web quando determinados rastreadores estão bloqueados, também adicionamos mensagens de aviso no console quando um controlador é bloqueado.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Mensagens no console quando o rastreamento de prevenção bloqueia o acesso ao armazenamento de um controlador  
:::image-end:::  

[Leia mais sobre a prevenção de rastreamento e o equilíbrio entre a compatibilidade entre privacidade e Web][TrackingPrevention].  

## Anúncios do projeto Chromium  

As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 81 que contribuíram para o projeto de código-fonte aberto Chromium.  

### Suporte do moto G4 no modo de dispositivo  

Depois de [habilitar a barra de ferramentas do dispositivo][DeviceToolbar], simule as dimensões de um visor moto G4 da lista de **dispositivos** .  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulando um visor moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Simulando um visor moto G4  
:::image-end:::  

Clique em [Mostrar quadro de dispositivo][DeviceFrame] para mostrar o hardware moto G4 em torno do visor.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrando o hardware moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Mostrando o hardware moto G4  
:::image-end:::  

Recursos relacionados:  

*   Abra o [menu de comando][CommandMenu] e execute o `Capture screenshot` comando para fazer uma captura de tela do visor que inclua o hardware moto G4 (após habilitar a **exibição do quadro de dispositivo**).  
*   [Acelera a rede e a CPU][ThrottleNetworkAndCpu] para simular com mais precisão as condições de navegação de um usuário móvel.  

Chromium problema [#924693][CR924693]  

### Atualizações relacionadas a cookies  

#### Cookies bloqueados no painel cookies  

O painel cookies no painel de aplicativos agora exibe cookies bloqueados com um plano de fundo amarelo.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueados no painel cookies do painel do aplicativo" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Cookies bloqueados no painel cookies do painel do aplicativo  
:::image-end:::  

Chromium problema [#1030258][CR1030258]  <!-- inaccessible  -->  

#### Prioridade do cookie no painel cookies  

As tabelas de cookies nos painéis rede e aplicativo agora incluem uma coluna de **prioridade** .  

> [!CAUTION]
> Navegadores baseados em Chromium, como o Microsoft Edge, são os únicos navegadores que dão suporte à prioridade de cookies.  

Chromium problema [#1026879][CR1026879]  

#### Editar todos os valores de cookies  

Todas as células nas tabelas de cookies são editáveis agora, exceto as células na coluna **tamanho** porque essa coluna representa o tamanho da rede do cookie, em bytes.  Veja os [campos][CookiesFields] para obter uma explicação de cada coluna.  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Editando um valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Editando um valor de cookie  
:::image-end:::  

#### Copiar como Node.js FETCH para incluir dados de cookies  

Clique com o botão direito do mouse em uma solicitação de rede e selecione **copiar**  >  **cópia como Node.js FETCH** para obter uma `fetch` expressão que inclua dados de cookies.  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js Fetch" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Copiar como Node.js Fetch  
:::image-end:::  

Chromium problema [#1029826][CR1029826]  

### Ícones mais precisos de manifesto do aplicativo Web  

Anteriormente, o painel de manifesto no painel do aplicativo enviou suas próprias solicitações para exibir os ícones de manifesto do aplicativo Web.  O DevTools agora mostra o mesmo ícone de manifesto usado pelo Microsoft Edge.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Ícones no painel manifestar" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Ícones no painel manifestar  
:::image-end:::  

Chromium problema [#985402][CR985402]  

### Passe o mouse sobre as propriedades do conteúdo CSS para ver os valores sem escape  

Passe o mouse sobre o valor de uma `content` propriedade para ver a versão sem escape do valor.  

Por exemplo, nesta [demonstração][CSSContentDemo] ao inspecionar o `p::after` pseudo elemento, você vê uma cadeia de caracteres de escape no painel estilos:  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="A cadeia de caracteres de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   A cadeia de caracteres de escape  
:::image-end:::  

Ao passar o mouse sobre o `content` valor, você vê o valor indesejado:  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="O valor não-escape" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   O valor não-escape  
:::image-end:::  

### Erros de mapa de origem mais detalhados no console  

Agora, o console fornece mais detalhes sobre o motivo pelo qual um mapa de origem falhou ao carregar ou analisar.  Anteriormente, era fornecido um erro sem explicar o que aconteceu de errado.  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Um erro de carregamento do mapa de origem no console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   Um erro de carregamento do mapa de origem no console  
:::image-end:::  

### Configuração para desativar a rolagem após o final de um arquivo  

Abra [configurações][Settings] e, em **Preferences**seguida, desabilite as  >  **fontes**  >  **de preferências permitem a rolagem do final do arquivo** para desativar o comportamento padrão da interface do usuário que permite rolar bem após o final de um arquivo no painel **fontes** .  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Desativando permitir rolagem após o final do arquivo" lightbox="../../images/2020/01/settings.msft.png":::
   Desativando **permitir rolagem após o fim do arquivo** em configurações  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="A rolagem após o final de um arquivo agora está desabilitada no painel fontes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   A rolagem após o final de um arquivo agora está desabilitada no painel fontes  
:::image-end:::  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge DevTools equipe  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular um visor móvel-simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Documentos da Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Show Device frame-simula dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Documentos da Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Acelerar a rede e a CPU-simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Documentos da Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Documentos da Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Campos: Exibir, editar e Excluir cookies com o Microsoft Edge DevTools | Documentos da Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para extensão de código do Microsoft Edge Visual Studio"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos para extensão de código do Microsoft Edge Visual Studio"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Código do Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \ (Chromium \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Melhorando a prevenção de rastreamento na postagem de blog do Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos do Microsoft Edge Insider"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Baixe o Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  

[CR924693]: https://crbug.com/924693 "Solicitação de recurso: Adicionar moto G4 à lista de modo de dispositivo | Erros de Chromium"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Erros de Chromium"  
[CR1026879]: https://crbug.com/1026879 "A guia cookies no console de desenvolvimento não mostra mais a prioridade | Erros de Chromium"  
[CR1029826]: https://crbug.com/1029826 "guia rede-> clique com o botão direito do mouse para solicitar-> copiar-> copiar como busca não copiar cookies | Erros de Chromium"  
[CR985402]: https://crbug.com/985402 "ícone de manifesto do aplicativo Web cadeias de caracteres de erro são confusas | Erros de Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com a WCAG | Erros de Chromium"  
[CR941561]: https://crbug.com/941561 "Possibilidade de localização do DevTools | Erros de Chromium"  
[CR987787]: https://crbug.com/987787 "Modo de exibição 3D dom | Erros de Chromium"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demonstração de conteúdo CSS não escape"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  

[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Informações sobre acessibilidade"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (modelo de objeto de documento) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-índice | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensão do navegador webhint | documentação do webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio extensão de código | documentação do webhint"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/01/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  