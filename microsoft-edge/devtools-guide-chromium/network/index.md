---
title: Inspecionar atividades de rede no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: cca9a45dae5ee845a219ef3f29c54a99e1ee904a
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985506"
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

1.  Abra a [demonstração][GlitchNetworkGetStarted]de introdução.  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       A demonstração  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  Para [abrir o devtools][DevToolsOpen] , pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  O painel **console** será aberto.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="O console" lightbox="../media/network-glitch-console.msft.png":::
       O **console**  
    :::image-end:::  
    
    Você pode preferir [encaixar devtools na parte inferior da janela][DevToolsCustomizePlacement].  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools encaixado na parte inferior da janela" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools encaixado na parte inferior da janela  
    :::image-end:::  
    
1.  Selecione a guia **rede** .  O painel rede é aberto.  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="DevTools encaixado na parte inferior da janela" lightbox="../media/network-glitch-network-bottom.msft.png":::
       DevTools encaixado na parte inferior da janela  
    :::image-end:::  
    
No momento, o painel de rede está vazio.  O DevTools somente registra a atividade de rede depois que você a abre e não ocorreu nenhuma atividade de rede desde que você tenha aberto o DevTools.  

## Registrar atividades de rede   

Para exibir a atividade de rede que uma página causa:  

1.  Recarregar a página.  O painel rede registra toda a atividade de rede no **log de rede**.  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="O log de rede" lightbox="../media/network-glitch-network.msft.png":::
       O **log de rede**  
    :::image-end:::  
    
    Cada linha do **log de rede** representa um recurso.  Por padrão, os recursos são listados cronologicamente.  O recurso superior geralmente é o principal documento HTML.  O recurso de baixo é o que foi solicitado por último.  
    
    Cada coluna representa informações sobre um recurso.  Na figura anterior, as colunas padrão são exibidas.  

    *   **Status**.  O código de status HTTP para resposta.  
    *   **Tipo**.  O tipo de recurso.  
    *   **Iniciador**.  A causa da solicitação do recurso.  Selecionar um link na coluna do iniciador leva você ao código-fonte que causou a solicitação.  
    *   **Tempo**.  A duração da solicitação.  
    *   **Cascata**.  Uma representação gráfica dos diferentes estágios da solicitação.  Passe o mouse sobre uma cascata para ver uma divisão.  
    
    > [!NOTE]
    > O gráfico acima do log de rede é chamado de visão geral.  Você não usará o gráfico de visão geral neste tutorial, portanto, poderá ocultá-lo.  Consulte [ocultar o painel Visão geral][DevtoolsReferenceHideOverview].
    
1.  Depois de abrir o DevTools, ele registra a atividade de rede no log de rede.  
    Para demonstrar isso, primeiro examine a parte inferior do **log de rede** e faça uma anotação mental da última atividade.  
1.  Agora, selecione o botão **obter dados** na demonstração.  
1.  Examine a parte inferior do **log de rede** novamente.  Você deve ver um novo recurso chamado `getstarted.json` .  Selecionar o botão **obter dados** fez com que a página solicitasse esse arquivo.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Um novo recurso no log de rede" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Um novo recurso no **log de rede**  
    :::image-end:::  
    
## Mostrar mais informações   

As colunas do log de rede são configuráveis.  Você pode ocultar colunas que não está usando.  
Também há muitas colunas que estão ocultas por padrão que podem ser úteis.  

1.  Clique com o botão direito do mouse no cabeçalho da tabela de log de rede e selecione **domínio**.  O domínio de cada recurso agora é mostrado.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Habilitar a coluna domínio" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Habilitar a coluna domínio  
    :::image-end:::  
    
    > [!TIP]
    > Veja a URL completa de um recurso passando o mouse sobre a célula na coluna **nome** .  
    
## Simular uma conexão de rede mais lenta   

A conexão de rede do computador que você usa para criar sites é provavelmente mais rápida do que as conexões de rede dos dispositivos móveis dos seus usuários.  Ao estreitar a página, você tem uma ideia melhor do tempo que uma página leva para ser carregada em um dispositivo móvel.  

1.  Selecione o menu suspenso **regulagem** , que é definido como **online** por padrão.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Habilitar limitação" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Habilitar limitação  
    :::image-end:::  
    
1.  Selecione **3G lento**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Selecionar 3G lento" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Selecionar 3G lento  
    :::image-end:::  
    
1.  Use o **recarregamento** de longa duração \ ( ![ recarregar ][ImageRefreshIcon] \) e, em seguida, selecione **esvaziar cache e Hard reload**.  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Esvaziar o cache e o recarregamento rígido" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Esvaziar o cache e o recarregamento rígido**  
    :::image-end:::  
    
    Em visitas de repetição, o navegador geralmente serve alguns arquivos do [cache][MDNHTTPCache], o que acelera a carga da página.  O **cache vazio e o recarregamento rígido** força o navegador a acessar a rede para todos os recursos.  Isso é útil quando você deseja ver como um visitante do primeiro visitante experimenta um carregamento de página.  
    
    > [!NOTE]
    > O fluxo de trabalho do **cache e do recarregamento de disco vazio** só está disponível quando o devtools está aberto.  
    
## Capturar capturas de tela   

As capturas de tela permitem ver como uma página é exibida ao longo do tempo durante o carregamento.  

1.  Selecione \ ( ![ configurações de rede ][ImageSettingsIcon] \) e marque a caixa de seleção **captura de tela de captura** .
1.  Recarregue a página novamente por meio do fluxo de trabalho do **cache vazio e do recarregamento de disco** .  Consulte [simular uma conexão mais lenta](#simulate-a-slower-network-connection) se você precisar de um lembrete sobre como fazer isso.  
    O painel capturas de tela fornece miniaturas de como a página examinou em vários pontos durante o processo de carregamento.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Capturas de tela do carregamento de página" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Capturas de tela do carregamento de página  
    :::image-end:::  
    
1.  Selecione a primeira miniatura.  O DevTools mostra o que a atividade de rede estava ocorrendo nesse momento.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="A atividade de rede que está acontecendo durante a primeira captura de tela" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       A atividade de rede que está acontecendo durante a primeira captura de tela  
    :::image-end:::  
    
1.  Selecione \ ( ![ configurações de rede ][ImageSettingsIcon] \) novamente e desmarque a caixa de seleção **capturar capturas de tela** para fechar o painel capturas de tela.
1.  Recarregue a página novamente.  
    
## Inspecionar os detalhes do recurso   

Selecione um recurso para saber mais sobre ele.  Experimente agora:  

1.  Selecione `getstarted.html` .  A guia **cabeçalhos** é mostrada.  Use esta guia para inspecionar cabeçalhos HTTP.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="A guia cabeçalhos" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       A guia **cabeçalhos**  
    :::image-end:::  
    
1.  Selecione a guia **Visualizar** .  Uma renderização básica do HTML é mostrada.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="A guia Visualização" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       A guia **Visualização**  
    :::image-end:::  
    
    Esta guia é útil quando uma API retorna um código de erro em HTML.  Pode ser mais fácil ler o HTML renderizado do que o código-fonte HTML ou ao inspecionar imagens.  

1.  Selecione a guia **resposta** .  O código-fonte HTML é mostrado.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="A guia resposta" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       A guia **resposta**  
    :::image-end:::  
    
    > [!TIP]
    > Quando um arquivo é minified, selecionar o **formato** \ ( ![ formato ][ImageFormatIcon] \) na parte inferior da guia **resposta** reformata novamente o conteúdo do arquivo para facilitar a leitura.  
    
1.  Selecione a guia **intervalo** .  Uma divisão da atividade de rede desse recurso é mostrada.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="A guia intervalo" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       A guia **intervalo**  
    :::image-end:::  
    
1.  Selecione **fechar** \ ( ![ fechar ][ImageCloseIcon] \) para exibir o log de rede novamente.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="O botão fechar" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       O botão **fechar**  
    :::image-end:::  
    
## Pesquisar cabeçalhos e respostas de rede   

Use o painel **Pesquisar** quando você precisar pesquisar os cabeçalhos HTTP e as respostas de todos os recursos para uma determinada cadeia de caracteres ou expressão regular.  

Por exemplo, suponha que você queira verificar se seus recursos estão usando **políticas de cache**razoáveis.  

<!--TODO: add cache policies section when available  -->

1.  Selecione **Pesquisar** \ ( ![ localizar ][ImageSearchIcon] \).  O painel Pesquisar é aberto à esquerda do log de rede.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Painel de pesquisa" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Painel de **pesquisa**  
    :::image-end:::  
    
1.  Digite `Cache-Control` e pressione `Enter` .  O painel Pesquisar lista todas as ocorrências `Cache-Control` que ele encontra em cabeçalhos ou conteúdo do recurso.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Resultados da pesquisa para Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Resultados da pesquisa‎‏ para  `Cache-Control`  
    :::image-end:::  
    
1.  Selecione um resultado para exibir o recurso no qual o resultado foi encontrado.  Se você estiver vendo os detalhes do recurso, selecione um resultado para ir diretamente para ele.  Por exemplo, se a consulta foi encontrada em um cabeçalho, a guia cabeçalhos será aberta.   Se a consulta foi encontrada em conteúdo, a guia **resposta** é aberta.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Um resultado da pesquisa realçado na guia cabeçalhos" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Um resultado da pesquisa realçado na guia **cabeçalhos**  
    :::image-end:::  
    
1.  Feche o painel Pesquisar e a guia cabeçalhos.  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Os botões fechar" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Os botões **fechar**  
    :::image-end:::  
    
## Filtrar recursos   

O DevTools oferece vários fluxos de trabalho para a filtragem de recursos que não são relevantes para a tarefa em questão.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="A barra de ferramentas filtros" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   A barra de ferramentas **filtros**  
:::image-end:::  

A barra de ferramentas **filtros** deve ser habilitada por padrão.  Se não:  

1.  Selecione **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para mostrá-lo.  
    
### Filtrar por cadeia de caracteres, expressão regular ou propriedade   

A caixa de texto **Filtrar** oferece suporte a muitos tipos diferentes de filtragem.  

1.  Digite `png` na caixa de texto **filtro** .  Somente os arquivos que contêm o texto `png` são exibidos.  Nesse caso, os únicos arquivos que correspondem ao filtro são as imagens PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Um filtro de cadeia de caracteres" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Um filtro de cadeia de caracteres  
    :::image-end:::  
    
1.  Digite `/.*\.[cj]s+$/`.  O DevTools filtra qualquer recurso com um nome de arquivo que não termina com um `j` ou um `c` seguido de 1 ou mais `s` caracteres.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Um filtro de expressão regular" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Um filtro de expressão regular  
    :::image-end:::  
    
1.  Digite `-main.css`.  DevTools filtros desconectados `main.css` .  Se qualquer outro arquivo coincidir com o padrão, ele também será filtrado.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Um filtro negativo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Um filtro negativo  
    :::image-end:::  
    
1.  Digite `domain:cdn.glitch.com` na caixa de texto **filtro** .  O DevTools filtra qualquer recurso com uma URL que não corresponde a este domínio.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Um filtro de propriedade" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Um filtro de propriedade  
    :::image-end:::  
    
    Consulte [Filtrar solicitações por Propriedades][DevtoolsReferenceProperty] para obter a lista completa de propriedades filtráveis.  
    
1.  Desmarque a caixa de texto **Filtrar** de qualquer texto.  
    
### Filtrar por tipo de recurso   

Para se concentrar em um determinado tipo de arquivo, como folhas de estilos:  

1.  Selecione **CSS**.  Todos os outros tipos de arquivo são filtrados.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Mostrar somente arquivos CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Mostrar somente arquivos CSS  
    :::image-end:::  
    
1.  Para ver também os scripts, segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e selecione **js**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Mostrar somente arquivos CSS e JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Mostrar somente arquivos CSS e JS  
    :::image-end:::  
    
1.  Selecione **tudo** para remover os filtros e ver todos os recursos novamente.  
    
Consulte [Filtrar solicitações][DevtoolsNetworkReferenceFilter] para outros fluxos de trabalho de filtragem.  

## Bloquear solicitações   

Qual a aparência de uma página e comportamento quando alguns dos recursos da página não estão disponíveis?  Ele falha completamente, ou ainda é um pouco funcional?  Bloquear solicitações para descobrir:  

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="O menu de comando" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Tipo `block` , selecione **Mostrar bloqueio de solicitação**e pressione `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Mostrar bloqueio de solicitações" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Mostrar bloqueio de solicitações**  
    :::image-end:::  
    
1.  Selecione **Adicionar padrão** \ ( ![ Adicionar padrão ][ImageAddIcon] \).  
1.  Digite `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Bloqueando Main. css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Pedi `main.css`  
    :::image-end:::  
    
1.  Selecione **Adicionar**.  
1.  Recarregar a página.  Como esperado, o estilo da página é levemente bagunçado porque a folha de estilos principal foi bloqueada.  
    
    > [!NOTE]
    > A `main.css` linha no log de rede.  O texto vermelho significa que o recurso foi bloqueado.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Main. CSS foi bloqueado" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` foi bloqueado  
    :::image-end:::  
    
1.  Desmarque a caixa de seleção **habilitar o bloqueio de solicitações** .  

## Conclusão  

Parabéns, você concluiu o tutorial.  Agora você sabe como usar o painel **rede** no Microsoft Edge devtools!

<!--




-->  

Confira a [referência de rede][DevtoolsNetworkReference] para descobrir mais recursos do devtools relacionados à atividade de inspeção da rede.  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Referência de análise de rede | Documentos da Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Filtrar solicitações-referência de análise de rede | Documentos da Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar o painel Visão geral-referência de análise de rede | Documentos da Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitações por Propriedades-referência de análise de rede | Documentos da Microsoft"
[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com o Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspecionar a demonstração da atividade de rede | Problema"  

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
