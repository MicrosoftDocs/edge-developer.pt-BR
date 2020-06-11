---
title: O que há de novo no DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7651430c581346d1f140f0a5974b8aa9bb809204
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708967"
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

# O que há de novo no DevTools (Microsoft Edge 83)  

Após o cronograma atualizado do Chromium, estamos ajustando o nosso cronograma para futuras versões do Microsoft Edge e cancelando o lançamento do Microsoft Edge 82. Confira nossa [postagem no blog][WindowsBlogStableRelease] para obter mais informações.  

Estes são os novos recursos disponíveis no DevTools no Microsoft Edge 83.  

## Anúncios da equipe do Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools! Dê uma olhada neles para experimentar os novos recursos do DevTools, as extensões de código do VS e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### Depurar remotamente o Microsoft Edge em dispositivos Windows 10  

O aplicativo [ferramentas remotas para Microsoft Edge \ (beta \)][RemoteTools] agora está disponível na [Microsoft Store][MicrosoftStore].  Ao usar este aplicativo, que estende o [Windows Device portal][WindowsDevicePortal], você pode se conectar da instância do Microsoft Edge em execução na sua máquina de desenvolvimento a um dispositivo Windows 10 remoto, ver uma lista de destinos \ (todas as guias no Microsoft Edge e [PWAs][PWADoc] abertas no dispositivo Windows 10 \) e usar o devtools em seu computador de desenvolvimento em relação a um destino em execução no dispositivo Windows 10 remoto.  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="O aplicativo Remote Tools para Microsoft Edge (beta) disponível na Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   Figura 1: o aplicativo [ferramentas remotas para o Microsoft Edge (beta)][RemoteTools] disponível na [Microsoft Store][MicrosoftStore]  
:::image-end:::  

[Leia nosso guia para configurar seu dispositivo Windows 10 e seu computador de desenvolvimento para depuração remota][RemoteDebuggingWin10].  Informe-nos sobre sua experiência de depuração remota em [tweet][PostTweetEdgeDevTools] ou clique no ícone de [comentários](#feedback) !  

### Novas maneiras de acessar as configurações  

Há toneladas de configurações para o DevTools que você pode personalizar para fazer com que a aparência DevTools e funcione da maneira que você precisa. No Microsoft Edge 83, agora é muito mais fácil acessar [as configurações][OverviewSettings] no devtools. Abra configurações com o ícone de engrenagem ao lado de alertas do console e o menu principal.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="O ícone de engrenagem abre as configurações na DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   Figura 2: o ícone de engrenagem abre **as configurações** na devtools  
:::image-end:::  

Você também pode abrir [as configurações][OverviewSettings] no **menu principal** em **mais ferramentas**.

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu principal > mais ferramentas > configurações" lightbox="../../media/2020/03/settings2.msft.png":::
   Figura 3: **menu principal**  >  **mais**  >  **configurações** de ferramentas  
:::image-end:::  

Chromium problema [#1050855][crbug1050855]

### Novo e aprimorado infobars

As barras de notificação informativas \ (infobars \) no DevTools agora têm uma aparência aprimorada e mais funcionalidades. No Microsoft Edge 83, o infobars é mais fácil de ler e oferecer botões para que você possa executar a ação relevante imediatamente.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barra de formatação para imprimir um arquivo minified no Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Figura 4: barra de formatação para imprimir um arquivo minified no Microsoft Edge versão 83  
:::image-end:::  

Chromium problema [#1056348][crbug1056348]

### Navegar pelo seletor de cores com o teclado  

O [seletor de cores][ColorPicker] é uma GUI no [painel elementos][ElementsDoc] para alteração `color` e `background-color` declarações.  Em versões anteriores do Microsoft Edge, você não pôde navegar na seção **sombras** do [seletor de cores][ColorPicker] com o teclado.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Agora você pode usar o teclado para mover o seletor na seção sombras do seletor de cores" lightbox="../../media/2020/03/color-picker.msft.png":::
   Figura 5: agora você pode usar o teclado para mover o seletor na seção **sombras** do [seletor de cores][ColorPicker]  
:::image-end:::  

No Microsoft Edge 83, agora você pode usar o teclado para mover o seletor na seção **sombras** do seletor de cores.  

Chromium problema [#963183][crbug963183]  

### A guia Propriedades agora é preenchida após uma atualização de página  

No Microsoft Edge 81 e versões anteriores, a **guia Propriedades** no [painel elementos][ElementsDoc] foi interrompida pelas atualizações de página.  Quando você atualiza a página, a **guia Propriedades** não preenche as propriedades do elemento atualmente selecionado.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="No Microsoft Edge 81 e versões anteriores, a guia Propriedades estava em branco após uma atualização de página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   Figura 6: no Microsoft Edge 81 e versões anteriores, a **guia Propriedades** estava em branco após uma atualização de página  
:::image-end:::  

No Microsoft Edge 83, agora você pode ver as propriedades do elemento atualmente selecionado após uma atualização de página na **guia Propriedades**.  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="No Microsoft Edge 83, a guia Propriedades exibe as propriedades do elemento atualmente selecionado após uma atualização de página" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   Figura 7: no Microsoft Edge 83, a **guia Propriedades** exibe as propriedades do elemento atualmente selecionado após uma atualização de página  
:::image-end:::  

Chromium problema [#1050999][crbug1050999]  

### Use as teclas de direção para rolar a ferramenta alterações  

A **ferramenta alterações** acompanha todas as alterações feitas em CSS ou JavaScript no devtools.  Você pode usar a ferramenta de **alterações** para ver rapidamente todas as suas alterações e retomar os retornos do seu editor/IDE.  

Para abrir a **ferramenta alterações** , pressione `Ctrl` + `Shift` + `P` a devtools para abrir o [menu de comandos][DevToolsCommandMenuIndex] e digite `changes` .  Selecione e execute o comando **Mostrar alterações** para abrir a **ferramenta mudanças** na gaveta do devtools.  

Quando você faz uma alteração em um arquivo minified, a **ferramenta alterações** permite que você role horizontalmente para ver todo o código do minified.  A partir do Microsoft Edge 83, agora você pode rolar horizontalmente usando as teclas de direção do teclado.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de direção para ver o código minified na ferramenta alterações" lightbox="../../media/2020/03/changes.msft.png":::
   Figura 8: no Microsoft Edge 83, você pode rolar horizontalmente com as teclas de direção para ver as alterações feitas em seu código minified na **ferramenta alterações**  
:::image-end:::  

Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone de [comentários](#feedback) !  

Chromium problema [#963183][crbug963183]  

## Anúncios do projeto Chromium  

As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 83 que contribuíram para o projeto de código-fonte aberto Chromium.  

### Emular deficiências de visão  

Abra a [guia renderização][RenderingDoc] e use o novo recurso de **deficiências de visão de emulação** para ter uma ideia melhor de como as pessoas com diferentes tipos de deficiência visual apresentam o seu site.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulando a visão desfocada" lightbox="../../media/2020/03/vision.msft.png":::
   Figura 9: emulando a visão desfocada  
:::image-end:::  

O DevTools é capaz de emular a visão borrada e os seguintes [tipos de deficiências de visão de cor][ColorBlindnessTypes].  

| Deficiência de visão colorida | Detalhes |  
|:--- |:--- |  
| Protanopia | A incapacidade de perceber qualquer luz vermelha. |  
| Deuteranopia | A incapacidade de perceber qualquer luz verde. |  
| Tritanopia | A incapacidade de perceber qualquer luz azul. |  
| Achromatopsia | A incapacidade de perceber qualquer cor, exceto para tonalidades de cinza \ (extremamente raro \). |  

Existem versões menos extremas dessas deficiências de visão de cor e, na verdade, são mais comuns.  
Por exemplo, protanomaly é uma sensibilidade reduzida à luz vermelha (em oposição ao protanopia, que é a incapacidade completa de perceber a luz vermelha). No entanto, essas deficiências de visão omaly não são tão claramente definidas: todas as pessoas com tal deficiência visual são diferentes e podem ver coisas de forma diferente (sendo capaz de perceber mais/menos das cores relevantes).  

Ao projetar para as simulações mais extremas no DevTools, os seus aplicativos Web são garantidos para pessoas com o protanomaly, o deuteranomaly, o tritanomaly e o achromatomaly também.  

Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !  

Chromium problema [#1003700][crbug1003700]  

### Emular localidades  

Emular localidades definindo um local no local dos **sensores**  >  **Location**. [Abrir o **menu de comando** ][DevToolsCommandMenuIndex] e digitar `Sensors` para acessar a guia **sensores** .  Depois de executar essas ações, o DevTools modifica a localidade padrão atual, afetando o código a seguir.  

*   `Intl.*` APIs, por exemplo: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Outras APIs JavaScript com reconhecimento de localidade, como `String.prototype.localeCompare` e `*.prototype.toLocaleString` , por exemplo: `123_456..toLocaleString()`  
*   APIs DOM, como `navigator.language` e `navigator.languages`  
*   O [`Accept-Language`][MDNAcceptLanguage] cabeçalho da solicitação http  

> [!NOTE]
> Atualizações `navigator.language` e `navigator.languages` não são visíveis imediatamente, mas somente após a próxima navegação ou página ser recarregadas.  As alterações feitas no `Accept-Language` cabeçalho http só se refletem nas solicitações subsequentes.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulando uma localidade" lightbox="../../media/2020/03/locale.msft.png":::
   Figura 10: emulando uma localidade  
:::image-end:::  

Para experimentar uma demonstração, consulte [exemplo de código dependente de localidade][MathiasByensLocaleDemo].

Chromium problema [#1051822][crbug1051822]

### Depuração de política de incorporação de várias origens (COEP)  

O painel rede agora fornece informações de depuração da [política de incorporação de várias origens][COEP] .  

A coluna **status** agora fornece uma explicação rápida do motivo pelo qual uma solicitação foi bloqueada, bem como um link para exibir os cabeçalhos dessa solicitação para a depuração adicional:  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitações bloqueadas na coluna * * status * *" lightbox="../../media/2020/03/status.msft.png":::
   Figura 11: solicitações bloqueadas na coluna status  
:::image-end:::  

A seção de **cabeçalhos de resposta** da guia **cabeçalhos** fornece mais orientações sobre como resolver os problemas:  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Mais diretrizes na seção cabeçalhos de resposta" lightbox="../../media/2020/03/guidance.msft.png":::
   Figura 12: mais diretrizes na seção de cabeçalhos de resposta  
:::image-end:::  

Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !  

Chromium problema [#1051466][crbug1051466]  

### Exibir solicitações de rede que definem um caminho de cookie específico  

Use a nova `cookie-path` palavra-chave Filter no painel **rede** para se concentrar nas solicitações de rede que definem um [caminho de cookie][MDNCookiePath]específico.  

Verifique as [solicitações de filtro por Propriedades][NetworkProperties] para descobrir mais palavras-chave como `cookie-path` .

### Encaixar à esquerda no menu de comando  

Abra o [menu de comando][DevToolsCommandMenuIndex] e execute o `Dock to left` comando para mover devtools para a esquerda do visor.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools encaixado à esquerda da viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   Figura 13: DevTools encaixado à esquerda da viewport  
:::image-end:::  

> [!NOTE]
> O recurso **Dock to Left** está disponível desde o Microsoft Edge 75, mas anteriormente era acessível apenas a partir do [**menu principal**][MainMenuDoc].  O novo recurso no Microsoft Edge 83 é que agora você pode acessar esse recurso no menu de comando.  

Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !  

Chromium problema [#1011679][crbug1011679]  

### O painel auditorias agora é o painel Lighthouse  

A equipe do DevTools freqüentemente tem comentários dos desenvolvedores da Web que, enquanto era possível executar o [Lighthouse][GithubGoogleChromeLighthouse] do devtools, quando eles tentavam não puderam localizar o painel "Lighthouse", portanto, o painel **auditorias** agora é o painel **Lighthouse** .  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="O painel Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Figura 14: painel de Lighthouse  
:::image-end:::  

> [!NOTE]
> O painel **Lighthouse** fornece links para conteúdo hospedado em websites de terceiros.  A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e todos os dados que eles podem coletar.  

### Excluir todas as substituições locais em uma pasta  

Depois de configurar **substituições locais** , você pode clicar com o botão direito do mouse em uma pasta e selecionar a opção novo **excluir tudo substitui** para excluir todas as substituições locais nessa pasta.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Excluir todas as substituições" lightbox="../../media/2020/03/overrides.msft.png":::
   Figura 15: excluir todas as substituições  
:::image-end:::  

Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !  

Chromium problema [#1016501][crbug1016501]  

### Interface do usuário de tarefas longa atualizada  

Uma **tarefa longa** é o código JavaScript que monopolizes o thread principal há muito tempo, fazendo com que uma página da Web congele.  

Você foi capaz de [Visualizar tarefas longas no painel de desempenho][LongTasksInPerformancePanel] durante um período de tempo, mas no Microsoft Edge 83 a interface do usuário de visualização de tarefa longa no painel desempenho foi atualizada.  A parte de tarefa longa de uma tarefa está agora colorida com um plano de fundo vermelho listrado.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="A nova interface do usuário de tarefa longa" lightbox="../../media/2020/03/long-task.msft.png":::
   Figura 16: a nova interface do usuário longa da tarefa  
:::image-end:::  

Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !  

Chromium problema [#1054447][crbug1054447]  

### Suporte a ícones mascaráveis no painel manifesto  

O Android Oreo introduziu ícones adaptáveis, que exibem ícones do aplicativo em uma variedade de formas em diferentes modelos de dispositivo.  **Ícones Mascaráveis** são um novo formato de ícone que dão suporte a ícones adaptáveis, que permitem que você verifique se o ícone do [PWA][PWADoc] tem uma boa aparência em dispositivos que dão suporte ao padrão de ícones mascaráveis.  

Habilite a caixa de seleção **Mostrar apenas a área de segurança mínima para ícones mascaráveis** no painel **manifesto** para verificar se o ícone mascarable tem uma boa aparência em dispositivos Android do Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="A caixa de seleção Mostrar apenas a área de segurança mínima para ícones mascaráveis" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   Figura 17: a caixa de seleção **Mostrar apenas a área de segurança mínima para ícones mascaráveis**  
:::image-end:::  

> [!NOTE]
> Este recurso foi iniciado no Microsoft Edge 81.  As atualizações abordadas aqui no Microsoft Edge 83 não foram abordadas nas novidades do [devtools (Microsoft edge 81)][WhatsNew81].  

## Privacidade Jurídica  

Para discutir os novos recursos e alterações nesta postagem, ou qualquer outro item relacionado ao DevTools:  

*   Envie seus comentários usando o ícone de **comentários** no devtools  
*   Tweet em [@EdgeDevTools][PostTweetEdgeDevTools]  
*   Enviar uma sugestão para [a Web que][TheWebWeWant] queremos  
*   Arquivos com erros neste documento no repositório [Edge-Developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue]  

:::image type="complex" source="../../media/2020/03/feedback-icon.msft.png" alt-text="O ícone * * feedback * * na Microsoft Edge DevTools" lightbox="../../media/2020/03/feedback-icon.msft.png":::
   Figura 18: o ícone de **comentários** no Microsoft Edge devtools  
:::image-end:::  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "O que há de novo no DevTools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Alterar as cores com o seletor de cores"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Alterar o posicionamento a partir do menu principal"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Exibir atividade de thread principal"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia renderização"  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introdução à depuração remota de dispositivos Windows 10"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Pontos de interrupção de linha do código"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Visão geral do Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Ferramentas remotas para Microsoft Edge (beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Atualização em lançamentos de canais estáveis para o Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Tipos de cegueira para cor"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemplo de código dependente de localidade"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Problema 963183: DevTools não são compatíveis com a WCAG"  
[crbug1003700]: https://crbug.com/1003700 "Problema 1003700: adicionar suporte a DevTools para simulação de deficiência visual de cor"  
[crbug1011679]: https://crbug.com/1011679 "Problema 1011679: apresentar ' Dock to Left ' usando o menu de comandos"  
[crbug1016501]: https://crbug.com/1016501 "Problema 1016501: solicitação de recurso: botão para excluir todas as substituições locais"  
[crbug1050999]: https://crbug.com/1050999 "Problema 1050999: guia Propriedades"  
[crbug1051466]: https://crbug.com/1051466 "Problema 1051466: suporte para a depuração COOP/COEP no DevTools"  
[crbug1054447]: https://crbug.com/1054447 "Problema 1054447: atualizar as métricas de desempenho na linha do tempo do DevTools"  
[crbug1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: adicionar a interface do usuário para emular a localidade"
[crbug1041830]: https://crbug.com/1041830 "Problema 1041830: aprimorar as cores dos pontos de interrupção"
[crbug1050855]: https://crbug.com/1050855 "Problema 1050855: o modo de exibição de configurações é difícil de descobrir"
[crbug1056348]: https://crbug.com/1056348 "Problema 1056348: atualização do componente da barra de atualizações"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP e COEP explicou-política do Opener entre origens"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP e COEP explicou-política de incorporação de várias origens"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Repositório do GitHub Lighthouse"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/03/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
