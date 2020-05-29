---
title: Inspecionar atividades de rede no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611809"
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





# Inspecionar atividades de rede no Microsoft Edge DevTools   



Este é um tutorial prático de alguns dos recursos DevTools mais usados relacionados à inspeção de atividades da rede para uma página.  

Consulte [referência de rede][DevtoolsNetworkReference] , se você quiser procurar recursos.  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## Quando usar o painel de rede   

Em geral, use o painel de rede quando precisar ter certeza de que os recursos estão sendo baixados ou carregados como esperado.  Os casos de uso mais comuns do painel rede são:  

*   Garantir que os recursos estejam realmente sendo carregados ou baixados.  
*   Inspecionar as propriedades de um recurso individual, como cabeçalhos HTTP, conteúdo, tamanho e assim por diante.  

Se você estiver procurando maneiras de melhorar o desempenho do carregamento de página, **não** comece com o painel de rede.  Há muitos tipos de problemas de desempenho de carga que não estão relacionados à atividade de rede.  Comece com o painel auditorias porque ele fornece sugestões direcionadas sobre como melhorar sua página.  Consulte [otimizar a velocidade do site][DevtoolsSpeedGetStarted].  

## Abrir o painel rede   

Para aproveitar ao máximo este tutorial, abra a demonstração e experimente os recursos na página de demonstração.  

1.  Abra a [demonstração][GlitchNetworkGetStarted] de introdução.  
    
    > ##### Figura 1  
    > A demonstração  
    > ![A demonstração][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  Para [abrir o devtools][DevToolsOpen] , pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  O painel **console** será aberto.  
    
    > ##### Figura 2  
    > O console  
    > ! [O console] [ImagesTutorialConsole]  
    
    Você pode preferir [encaixar devtools na parte inferior da janela][DevToolsCustomizePlacement].  
    
    > ##### Figura 3  
    > DevTools encaixado na parte inferior da janela  
    > ! [DevTools encaixado na parte inferior da janela] [ImagesTutorialDocked]  

1.  Selecione a guia **rede** .  O painel rede é aberto.  
    
    > ##### Figura 4  
    > DevTools encaixado na parte inferior da janela  
    > ! [DevTools encaixado na parte inferior da janela] [ImagesTutorialNetwork]  

No momento, o painel de rede está vazio.  O DevTools somente registra a atividade de rede depois que você a abre e não ocorreu nenhuma atividade de rede desde que você tenha aberto o DevTools.  

## Registrar atividades de rede   

Para exibir a atividade de rede que uma página causa:  

1.  Recarregar a página.  O painel rede registra toda a atividade de rede no **log de rede**.  
    
    > ##### Figura 5  
    > O log de rede  
    > ! [O log de rede] [ImagesTutorialLog]  
    
    Cada linha do **log de rede** representa um recurso.  Por padrão, os recursos são listados cronologicamente.  O recurso superior geralmente é o principal documento HTML.  O recurso de baixo é o que foi solicitado por último.  
    
    Cada coluna representa informações sobre um recurso.  A [**Figura 6**](#figure-6) mostra as colunas padrão:  

    *   **Status**.  O código de status HTTP para resposta.  
    *   **Tipo**.  O tipo de recurso.  
    *   **Iniciador**.  A causa da solicitação do recurso.  Selecionar um link na coluna do iniciador leva você ao código-fonte que causou a solicitação.  
    *   **Tempo**.  A duração da solicitação.  
    *   **Cascata**.  Uma representação gráfica dos diferentes estágios da solicitação.  
        Passe o mouse sobre uma cascata para ver uma divisão.  
    
    > [!NOTE]
    > O gráfico acima do log de rede é chamado de visão geral.  Você não usará o gráfico de visão geral neste tutorial, portanto, poderá ocultá-lo.  Consulte [ocultar o painel Visão geral][DevtoolsReferenceHideOverview].
        
1.  Depois de abrir o DevTools, ele registra a atividade de rede no log de rede.  
    Para demonstrar isso, primeiro examine a parte inferior do **log de rede** e faça uma anotação mental da última atividade.  
1.  Agora, selecione o botão **obter dados** na demonstração.  
1.  Examine a parte inferior do **log de rede** novamente.  Você deve ver um novo recurso chamado `getstarted.json` .  Selecionar o botão **obter dados** fez com que a página solicitasse esse arquivo.  
    
    > ##### Figura 6  
    > Um novo recurso no log de rede  
    > ! [Um novo recurso no log de rede] [ImagesTutorialRuntime]  

## Mostrar mais informações   

As colunas do log de rede são configuráveis.  Você pode ocultar colunas que não está usando.  
Também há muitas colunas que estão ocultas por padrão que podem ser úteis.  

1.  Clique com o botão direito do mouse no cabeçalho da tabela de log de rede e selecione **domínio**.  O domínio de cada recurso agora é mostrado.  
    
    > ##### Figura 7  
    > Habilitando a coluna domínio  
    > ! [Habilitando a coluna de domínio] [ImagesTutorialDomain]  
    
    > [!TIP]
    > Veja a URL completa de um recurso passando o mouse sobre a célula na coluna **nome** .  

## Simular uma conexão de rede mais lenta   

A conexão de rede do computador que você usa para criar sites é provavelmente mais rápida do que as conexões de rede dos dispositivos móveis dos seus usuários.  Ao estreitar a página, você tem uma ideia melhor do tempo que uma página leva para ser carregada em um dispositivo móvel.  

1.  Selecione o menu suspenso **regulagem** , que é definido como **online** por padrão.  
    
    > ##### Figura 8  
    > Habilitando a limitação  
    > ! [Habilitando limitação] [ImagesTutorialThrottling]  
    
1.  Selecione **3G lento**.  
    
    > ##### Figura 9  
    > Seleção de 3G lento  
    > ! [Seleção de 3G lento] [ImagesTutorialSlow3G]  
    
1.  Longo **-pressione a recarga do** recarregamento ![ ][ImageRefreshIcon] e selecione **esvaziar cache e recarregamento físico**.  
    
    > ##### Figura 10  
    > Esvaziar o cache e o recarregamento rígido  
    > ! [Esvaziar o cache e o recarregamento de disco rígido] [ImagesTutorialHardReload]  
    
    Em visitas de repetição, o navegador geralmente serve alguns arquivos do [cache][MDNHTTPCache] , o que acelera a carga da página.  O **cache vazio e o recarregamento rígido** força o navegador a acessar a rede para todos os recursos.  Isso é útil quando você deseja ver como um visitante do primeiro visitante experimenta um carregamento de página.  
    
    > [!NOTE]
    > O fluxo de trabalho do **cache e do recarregamento de disco vazio** só está disponível quando o devtools está aberto.  

## Capturar capturas de tela   

As capturas de tela permitem ver como uma página é exibida ao longo do tempo durante o carregamento.  

1.  Selecione ![ configurações ][ImageSettingsIcon] de rede e marque a caixa de seleção **captura de tela de captura** .
1.  Recarregue a página novamente por meio do fluxo de trabalho do **cache vazio e do recarregamento de disco** .  Consulte [simular uma conexão mais lenta](#simulate-a-slower-network-connection) se você precisar de um lembrete sobre como fazer isso.  
    O painel capturas de tela fornece miniaturas de como a página examinou em vários pontos durante o processo de carregamento.  
    
    > ##### Figura 11  
    > Capturas de tela do carregamento de página  
    > ! [Capturas de tela do carregamento da página] [ImagesTutorialAllScreenshots]  

1.  Selecione a primeira miniatura.  O DevTools mostra o que a atividade de rede estava ocorrendo nesse momento.  
    
    > ##### Figura 12  
    > A atividade de rede que está acontecendo durante a primeira captura de tela  
    > ! [A atividade de rede que estava acontecendo durante a primeira captura de tela] [ImagesTutorialFirstScreenshot]  

1.  Selecione ![ as configurações ][ImageSettingsIcon] de rede novamente e desmarque a caixa de seleção **capturar capturas de tela** para fechar o painel capturas de tela.
1.  Recarregue a página novamente.  

## Inspecionar os detalhes do recurso   

Selecione um recurso para saber mais sobre ele.  Experimente agora:  

1.  Selecione `getstarted.html` .  A guia **cabeçalhos** é mostrada.  Use esta guia para inspecionar cabeçalhos HTTP.  
    
    > ##### Figura 13  
    > A guia cabeçalhos  
    > ! [A guia cabeçalhos] [ImagesTutorialHeaders]  
    
1.  Selecione a guia **Visualizar** .  Uma renderização básica do HTML é mostrada.  
    
    > ##### Figura 14  
    > A guia Visualização  
    > ! [A guia Visualização] [ImagesTutorialPreview]  

     Esta guia é útil quando uma API retorna um código de erro em HTML.  Pode ser mais fácil ler o HTML renderizado do que o código-fonte HTML ou ao inspecionar imagens.  

1.  Selecione a guia **resposta** .  O código-fonte HTML é mostrado.  
    
    > ##### Figura 15  
    > A guia resposta  
    > ! [A guia resposta] [ImagesTutorialResponse]  
    
    > [!TIP]
    > Quando um arquivo é minified, **selecionar o** ![ botão Formatar formato ][ImageFormatIcon] na parte inferior da guia **resposta** reformata o conteúdo do arquivo para facilitar a leitura.  

1.  Selecione a guia **intervalo** .  Uma divisão da atividade de rede desse recurso é mostrada.  
    
    > ##### Figura 16  
    > A guia intervalo  
    > ! [A guia intervalo] [ImagesTutorialTiming]  

1.  Selecione **fechar** ![ fechar ][ImageCloseIcon] para exibir o log de rede novamente.  
    
    > ##### Figura 17  
    > O botão fechar  
    > ! [O botão fechar] [ImagesTutorialCloseTiming]  

## Pesquisar cabeçalhos e respostas de rede   

Use o painel **Pesquisar** quando você precisar pesquisar os cabeçalhos HTTP e as respostas de todos os recursos para uma determinada cadeia de caracteres ou expressão regular.  

Por exemplo, suponha que você queira verificar se seus recursos estão usando **políticas de cache**razoáveis.  

<!--TODO: add cache policies section when available  -->

1.  Selecione **Pesquisar** ![ pesquisa ][ImageSearchIcon] .  O painel Pesquisar é aberto à esquerda do log de rede.  
    
    > ##### Figura 18  
    > Painel de pesquisa  
    > ! [O painel Pesquisar] [ImagesTutorialSearch]  

1.  Digite `Cache-Control` e pressione `Enter` .  O painel Pesquisar lista todas as ocorrências `Cache-Control` que ele encontra em cabeçalhos ou conteúdo do recurso.  
    
    > ##### Figura 19  
    > Resultados da pesquisa‎‏ para  `Cache-Control`  
    > ! [Resultados da pesquisa para Cache-Control] [ImagesTutorialResults]  

1.  Selecione um resultado para exibir o recurso no qual o resultado foi encontrado.  Se você estiver vendo os detalhes do recurso, selecione um resultado para ir diretamente para ele.  Por exemplo, se a consulta foi encontrada em um cabeçalho, a guia cabeçalhos será aberta.   Se a consulta foi encontrada em conteúdo, a guia **resposta** é aberta.  
    
    > ##### Figura 20  
    > Um resultado da pesquisa realçado na guia cabeçalhos  
    > ! [Um resultado de pesquisa é realçado na guia cabeçalhos] [ImagesTutorialCache]  
    
1.  Feche o painel Pesquisar e a guia cabeçalhos.  
    
    > ##### Figura 21  
    > Os botões fechar  
    > ! [Os botões fechar] [ImagesTutorialCloseButtons]  
    
## Filtrar recursos   

O DevTools oferece vários fluxos de trabalho para a filtragem de recursos que não são relevantes para a tarefa em questão.  

> ##### Figura 22  
> A barra de ferramentas filtros  
> ! [A barra de ferramentas filtros] [ImagesTutorialFilters]  

A barra de ferramentas **filtros** deve ser habilitada por padrão.  Se não:  

1.  Selecione **Filter** ![ filtro ][ImageFilterIcon] de filtro para mostrá-lo.  

### Filtrar por cadeia de caracteres, expressão regular ou propriedade   

A caixa de texto **Filtrar** oferece suporte a muitos tipos diferentes de filtragem.  

1.  Digite `png` na caixa de texto **filtro** .  Somente os arquivos que contêm o texto `png` são exibidos.  Nesse caso, os únicos arquivos que correspondem ao filtro são as imagens PNG.  
    
    > ##### Figura 23  
    > Um filtro de cadeia de caracteres  
    > ! [Um filtro de cadeia de caracteres] [ImagesTutorialPNG]  

1.  Digite `/.*\.[cj]s+$/`.  O DevTools filtra qualquer recurso com um nome de arquivo que não termina com um `j` ou um `c` seguido de 1 ou mais `s` caracteres.  
    
    > ##### Figura 24  
    > Um filtro de expressão regular  
    > ! [Um filtro de expressão regular] [ImagesTutorialRegEx]  
    
1.  Digite `-main.css`.  DevTools filtros desconectados `main.css` .  Se qualquer outro arquivo coincidir com o padrão, ele também será filtrado.  
    
    > ##### Figura 25  
    > Um filtro negativo  
    > ! [Um filtro negativo] [ImagesTutorialNegative]  
    
1.  Digite `domain:cdn.glitch.com` na caixa de texto **filtro** .  O DevTools filtra qualquer recurso com uma URL que não corresponde a este domínio.  
    
    > ##### Figura 26  
    > Um filtro de propriedade  
    > ! [Um filtro de propriedade] [ImagesTutorialProperty]  

    Consulte [Filtrar solicitações por Propriedades][DevtoolsReferenceProperty] para obter a lista completa de propriedades filtráveis.  
    
    
1.  Desmarque a caixa de texto **Filtrar** de qualquer texto.  

### Filtrar por tipo de recurso   

Para se concentrar em um determinado tipo de arquivo, como folhas de estilos:  

1.  Selecione **CSS**.  Todos os outros tipos de arquivo são filtrados.  
    
    > ##### Figura 27  
    > Mostrando somente arquivos CSS  
    > ! [Mostrando somente arquivos CSS] [ImagesTutorialCSS]  
    
1.  Para ver também os scripts, segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e selecione **js**.  
    
    > ##### Figura 28  
    > Mostrando somente arquivos CSS e JS  
    > ! [Mostrar somente arquivos CSS e JS] [ImagesTutorialCSSJS]  
    
1.  Selecione **tudo** para remover os filtros e ver todos os recursos novamente.  

Consulte [Filtrar solicitações][DevtoolsNetworkReferenceFilter] para outros fluxos de trabalho de filtragem.  

## Bloquear solicitações   

Qual a aparência de uma página e comportamento quando alguns dos recursos da página não estão disponíveis?  Ele falha completamente, ou ainda é um pouco funcional?  Bloquear solicitações para descobrir:  

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    > ##### Figura 29  
    > O menu de comando  
    > ! [O menu de comando] [ImagesTutorialCommandMenu]  
    
1.  Tipo `block` , selecione **Mostrar bloqueio de solicitação**e pressione `Enter` .  
    
    > ##### Figura 30  
    > Mostrar bloqueio de solicitações  
    > ! [Mostrar bloqueio de solicitação] [ImagesTutorialBlock]  

1.  Selecione **Adicionar padrão** ![ Adicionar padrão ][ImageAddIcon] .  
1.  Digite `main.css`.  
    
    > ##### Figura 31  
    > Pedi `main.css`  
    > ! [Bloqueando Main. CSS] [ImagesTutorialAddBlock]  
    
1.  Selecione **Adicionar**.  
1.  Recarregar a página.  Como esperado, o estilo da página é levemente bagunçado porque a folha de estilos principal foi bloqueada.  
    
    > [!NOTE]
    > A `main.css` linha no log de rede.  O texto vermelho significa que o recurso foi bloqueado.
    
    > ##### Figura 32  
    > `main.css` foi bloqueado  
    > ! [Main. CSS foi bloqueado] [ImagesTutorialBlockedStyles]  

1.  Desmarque a caixa de seleção **habilitar o bloqueio de solicitações** .  

## Conclusão  

Parabéns, você concluiu o tutorial.  Agora você sabe como usar o painel rede no Microsoft Edge DevTools!






Confira a [referência de rede][DevtoolsNetworkReference] para descobrir mais recursos do devtools relacionados à atividade de inspeção da rede.  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Figura 1: a demonstração"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-console.msft.png "Figura 2: o console"  
[ImagesTutorialDocked]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-console-Bottom.msft.png "Figura 3: DevTools encaixado na parte inferior da janela"  
[ImagesTutorialNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Bottom.msft.png "Figura 4: DevTools encaixado na parte inferior da janela"  
[ImagesTutorialLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network.msft.png "Figura 5: o log de rede"  
[ImagesTutorialRuntime]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-New-Resource.msft.png "Figura 6: um novo recurso no log de rede"  
[ImagesTutorialDomain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Edit-Column.msft.png "Figura 7: Habilitando a coluna de domínio"  
[ImagesTutorialThrottling]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-throttling.msft.png "Figura 8: habilitação da limitação"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-throttling-Slow-3G.msft.png "Figura 9: seleção de 3G lento"  
[ImagesTutorialHardReload]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Empty-cache-and-Hard-Reset.msft.png "Figura 10: cache vazio e recarregamento de disco rígido"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots.msft.png "Figura 11: capturas de tela do carregamento da página"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots-First.msft.png "Figura 12: a atividade de rede que aconteceu durante a primeira captura de tela"  
[ImagesTutorialHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Headers.msft.png "Figura 13: a guia cabeçalhos"  
[ImagesTutorialPreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Preview.msft.png "Figura 14: a guia Visualizar"  
[ImagesTutorialResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Response.msft.png "Figura 15: a guia resposta"  
[ImagesTutorialTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-timing.msft.png "Figura 16: a guia intervalo"  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Close-Tabs.msft.png "figura 17: o botão fechar"  
[ImagesTutorialSearch]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Empty.msft.png "Figura 18: o painel Pesquisar"  
[ImagesTutorialResults]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control.msft.png "Figura 19: resultados da pesquisa para Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control-Headers-Response-Headers.msft.png "Figura 20: um resultado de pesquisa realçado na guia cabeçalhos"  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Close.msft.png "figura 21: os botões fechar"  
[ImagesTutorialFilters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Empty.msft.png "Figura 22: a barra de ferramentas filtros"  
[ImagesTutorialPNG]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-png.msft.png "Figura 23: um filtro de cadeia de caracteres"  
[ImagesTutorialRegEx]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Regex.msft.png "Figura 24: um filtro de expressão regular"  
[ImagesTutorialNegative]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Negative-Statement.msft.png "figura 25: um filtro negativo"  
[ImagesTutorialProperty]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Property-Value.msft.png "Figura 26: um filtro de propriedade"  
[ImagesTutorialCSS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS.msft.png "Figura 27: mostrando apenas arquivos CSS"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS-JS.msft.png "Figura 28: mostrando somente arquivos CSS e JS"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Empty.msft.png "figura 29: o menu de comando"  
[ImagesTutorialBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block.msft.png "figura 30: mostrar bloqueio de solicitações"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Add-Pattern.msft.png "figura 31: bloqueando Main. css"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Main-CSS.msft.png "Figura 32: Main. CSS foi bloqueado"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Referência de análise de rede"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Filtrar solicitações-referência de análise de rede"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Ocultar o painel Visão geral-referência de análise de rede"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitações por Propriedades-referência de análise de rede"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Otimizar a velocidade do site com o Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Demonstração de atividade da rede de inspeção"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Cache HTTP | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
