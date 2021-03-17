---
description: Um tutorial sobre os recursos relacionados à rede mais populares no Microsoft Edge DevTools.
title: Inspecionar a atividade de rede no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a4a552fa9a45267a6ffa4a4e83e7ebc4e1817162
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439693"
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

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a>Inspecionar a atividade de rede no Microsoft Edge DevTools  

Este é um tutorial prática de alguns dos recursos de DevTools mais usados relacionados à inspeção da atividade de rede para uma página.  

Se você quiser navegar por recursos, navegue até [Referência de Rede][DevtoolsNetworkReference].  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a>Quando usar o painel Rede  

Em geral, use o painel Rede quando precisar se certificar de que os recursos estão sendo baixados ou carregados conforme o esperado.  Os casos de uso mais comuns para o painel Rede são:  

*   Certifique-se de que os recursos realmente estão sendo carregados ou baixados.  
*   Inspecionando as propriedades de um recurso individual, como os cabeçalhos HTTP, conteúdo, tamanho e assim por diante.  
    
Se você estiver procurando maneiras de melhorar o desempenho da carga da página, **não comece** com a **ferramenta Rede.**  Há muitos tipos de problemas de desempenho de carga que não estão relacionados à atividade de rede.  Comece com o painel Auditorias porque ele fornece sugestões direcionadas sobre como melhorar sua página.  Navegue até [Otimizar Velocidade do Site.][DevtoolsSpeedGetStarted]  

## <a name="open-the-network-panel"></a>Abrir o painel Rede  

Para obter o máximo deste tutorial, abra a demonstração e experimente os recursos na página de demonstração.  

1.  Abra a [demonstração Get Started][GlitchNetworkGetStarted].  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="A demonstração" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       A demonstração  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  Para [Abrir DevTools,][DevToolsOpen]selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).  A **ferramenta Console** é aberta.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="O Console" lightbox="../media/network-glitch-console.msft.png":::
       O **Console**  
    :::image-end:::  
    
    Você pode preferir [acoplar o DevTools na parte inferior da janela.][DevToolsCustomizePlacement]  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools encaixado na parte inferior da janela" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools encaixado na parte inferior da janela  
    :::image-end:::  
    
1.  Abra a **ferramenta Rede.**  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Ferramenta de console no DevTools encaixado na parte inferior da janela" lightbox="../media/network-glitch-network-bottom.msft.png":::
       **Ferramenta de** console no DevTools encaixado na parte inferior da janela  
    :::image-end:::  
    
No momento, **a ferramenta Rede** está vazia.  O DevTools registra somente a atividade de rede depois de abri-la e nenhuma atividade de rede ocorreu desde que você abriu o DevTools.  

## <a name="log-network-activity"></a>Atividade de rede de log  

Para exibir a atividade de rede que uma página causa:  

1.  Atualize a página da Web.  O painel Rede registra todas as atividades de rede no **Log de Rede.**  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="O Log de Rede" lightbox="../media/network-glitch-network.msft.png":::
       O **Log de Rede**  
    :::image-end:::  
    
    Cada linha do **Log de Rede** representa um recurso.  Por padrão, os recursos são listados cronologicamente.  O recurso superior geralmente é o documento HTML principal.  O recurso inferior é o que foi solicitado por último.  
    
    Cada coluna representa informações sobre um recurso.  Na figura anterior, as colunas padrão são exibidas.  

    *   **Status**.  O código de status HTTP para resposta.  
    *   **Tipo**.  O tipo de recurso.  
    *   **Iniciador**.  A causa da solicitação de recurso.  CHoosing a link in the Initiator column takes you to the source code that caused the request.  
    *   **Hora**.  A duração da solicitação.  
    *   **Cascata**.  Uma representação gráfica dos diferentes estágios da solicitação.  Para exibir uma divisão, passe o mouse em uma Cascata.  
    
    > [!NOTE]
    > O gráfico acima do Log de Rede é chamado de Visão Geral.  Você não usará o gráfico Visão geral neste tutorial, portanto, pode escondê-lo.  Navegue [até Ocultar o painel Visão Geral.][DevtoolsReferenceHideOverview]
    
1.  Depois de abrir o DevTools, ele registra a atividade de rede no Log de Rede.  
    Para demonstrar isso, primeiro veja a parte inferior do Log de **Rede** e faça uma anotação mental da última atividade.  
1.  Agora, selecione o **botão Obter Dados** na demonstração.  
1.  Veja a parte inferior do **Log de Rede novamente.**  Um novo recurso chamado `getstarted.json` é exibido.  Para fazer com que a página da Web solicite o arquivo, escolha o **botão Obter Dados.**  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Um novo recurso no Log de Rede" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Um novo recurso no Log **de Rede**  
    :::image-end:::  
    
## <a name="show-more-information"></a>Mostrar mais informações  

As colunas do Log de Rede são configuráveis.  Você pode ocultar colunas que não está usando.  
Há também muitas colunas ocultas por padrão que você pode achar útil.  

1.  Passe o mouse no header da tabela Log de Rede, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Domínio**.  O domínio de cada recurso agora é mostrado.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Habilitar a coluna Domínio" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Habilitar a coluna Domínio  
    :::image-end:::  
    
    > [!TIP]
    > Para revisar a URL completa de um recurso, passe o mouse na célula na **coluna** Nome.  
    
## <a name="simulate-a-slower-network-connection"></a>Simular uma conexão de rede mais lenta  

A conexão de rede do computador que você usa para criar sites provavelmente é mais rápida do que as conexões de rede dos dispositivos móveis de seus usuários.  Ao throttling da página, você tem uma ideia melhor de quanto tempo uma página leva para carregar em um dispositivo móvel.  

1.  Escolha o **menu suspenso Throttling,** que é definido como **Online** por padrão.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Habilitar a throttling" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Habilitar a throttling  
    :::image-end:::  
    
1.  Escolha **Slow 3G**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Escolha Slow 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Escolha Slow 3G  
    :::image-end:::  
    
1.  Pressione Longa **carga** \( Recarregar \) e escolha ![ Cache Vazio e ](../media/refresh-icon.msft.png) **Recarregá-lo.**  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Cache vazio e recarregá-la" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Cache vazio e recarregá-la**  
    :::image-end:::  
    
    Em visitas repetidas, o navegador geralmente atende alguns arquivos do [cache][MDNHTTPCache], o que acelera o carregamento da página.  **O Cache Vazio e a Recarga Dura** forçam o navegador a ir para a rede para todos os recursos.  Use-o para exibir como um visitante de primeira vez experimenta uma carga de página.  
    
    > [!NOTE]
    > O **fluxo de trabalho DevTools** e Cache Vazio e Carga Dura só estará disponível quando o DevTools estiver aberto.  
    
## <a name="capture-screenshots"></a>Capturar capturas de tela  

Capturas de tela exibem a aparência de uma página da Web ao longo do tempo enquanto ela é carregada.  

1.  Escolha \( Configurações de rede \) e a caixa de seleção ![ ](../media/settings-icon.msft.png) Captura captura **capturas** de tela.
1.  Atualize a página novamente usando **o fluxo de trabalho de Cache Vazio e De Carregamento** Rígido.  Navegue [até Simular uma conexão mais](#simulate-a-slower-network-connection) lenta se precisar de um lembrete sobre como fazer isso.  
    O painel Capturas de Tela fornece miniaturas de como a página foi olhada em vários pontos durante o processo de carregamento.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Capturas de tela da carga da página" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Capturas de tela da carga da página  
    :::image-end:::  
    
1.  Escolha a primeira miniatura.  O DevTools mostra qual atividade de rede estava ocorrendo nesse momento no tempo.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="A atividade de rede que estava acontecendo durante a primeira captura de tela" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       A atividade de rede que estava acontecendo durante a primeira captura de tela  
    :::image-end:::  
    
1.  Escolha \( Configurações de rede \) novamente e desativar a caixa de seleção Captura capturas de tela para fechar o ![ ](../media/settings-icon.msft.png) painel Capturas de Tela. ****
1.  Atualize a página novamente.  
    
## <a name="inspect-the-details-of-the-resource"></a>Inspecionar os detalhes do recurso  

Escolha um recurso para saber mais sobre ele.  Experimente agora:  

1.  Escolha `getstarted.html` .  O **painel Headers** é mostrado.  Use este painel para inspecionar cabeçalhos HTTP.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="O painel Headers" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       O **painel Headers**  
    :::image-end:::  
    
1.  Escolha o **painel Visualização.**  Uma renderização básica do HTML é mostrada.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="O painel Visualização" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       O **painel Visualização**  
    :::image-end:::  
    
    O painel é útil quando uma API retorna um código de erro em HTML.  Você pode achar mais fácil ler o HTML renderizado do que o código-fonte HTML ou ao inspecionar imagens.  

1.  Escolha o **painel Resposta.**  O código-fonte HTML é mostrado.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="O painel Resposta" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       O **painel Resposta**  
    :::image-end:::  
    
    > [!TIP]
    > Quando um arquivo for minificado, escolha o botão **Formatar** \( Formatar \) na parte inferior do painel resposta para formatar o conteúdo do arquivo para capacidade ![ ](../media/format-icon.msft.png) de leitura. ****  
    
1.  Escolha o **painel Timing.**  Uma divisão da atividade de rede do recurso é exibida.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="O painel Timing" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       O **painel Timing**  
    :::image-end:::  
    
1.  Escolha **Fechar** \( ![ Fechar ](../media/close-icon.msft.png) \) para exibir o Log de Rede novamente.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="O botão Fechar" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       O **botão Fechar**  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a>Respostas e headers de rede de pesquisa  

Use o **painel** Pesquisar quando precisar pesquisar os cabeçalhos HTTP e respostas de todos os recursos para uma determinada cadeia de caracteres ou expressão regular.  

Por exemplo, suponha que você queira verificar se seus recursos estão usando políticas de **cache razoáveis.**  

<!--TODO: add cache policies section when available  -->

1.  Escolha **Pesquisar** \( ![ Pesquisar ](../media/search-icon.msft.png) \).  O painel Pesquisar é aberto à esquerda do log de rede.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="O painel Pesquisar" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       O **painel** Pesquisar  
    :::image-end:::  
    
1.  Digite `Cache-Control` e selecione `Enter` .  O painel Pesquisar lista todas as instâncias que encontra `Cache-Control` em headers de recursos ou conteúdo.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Resultados da pesquisa para Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Resultados da pesquisa‎‏ para  `Cache-Control`  
    :::image-end:::  
    
1.  Escolha um resultado para exibir o recurso no qual o resultado foi encontrado.  Se você estiver olhando para os detalhes do recurso, selecione um resultado para ir diretamente para ele.  Por exemplo, se a consulta foi encontrada em um header, o **painel Headers** será aberto.   Se a consulta foi encontrada no conteúdo, o **painel Resposta** será aberto.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Um resultado de pesquisa realçado no painel Headers" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Um resultado de pesquisa realçado no painel **Headers**  
    :::image-end:::  
    
1.  Feche o painel Pesquisa e o **painel Headers.**  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Os botões Fechar" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Os **botões Fechar**  
    :::image-end:::  
    
## <a name="filter-resources"></a>Filtrar recursos  

O DevTools fornece vários fluxos de trabalho para filtrar recursos que não são relevantes para a tarefa em questão.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="A barra de ferramentas Filters" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   A **barra de ferramentas Filters**  
:::image-end:::  

A **barra de** ferramentas Filters deve ser ativado por padrão.  Caso não seja:  

1.  Escolha **Filtrar** \( ![ ](../media/filter-icon.msft.png) Filtrar \) para exibi-lo.  
    
### <a name="filter-by-string-regular-expression-or-property"></a>Filtrar por cadeia de caracteres, expressão regular ou propriedade  

A **caixa de** texto Filtro oferece suporte a vários tipos diferentes de filtragem.  

1.  Digite `png` na caixa de **texto** Filtrar.  Somente os arquivos que contêm o texto `png` são mostrados.  Nesse caso, os únicos arquivos que corresponderem ao filtro são as imagens PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Um filtro de cadeia de caracteres" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Um filtro de cadeia de caracteres  
    :::image-end:::  
    
1.  Digite `/.*\.[cj]s+$/`.  O DevTools filtra qualquer recurso com um nome de arquivo que não termine com um ou um seguido `j` `c` de 1 ou mais `s` caracteres.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Um filtro de expressão regular" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Um filtro de expressão regular  
    :::image-end:::  
    
1.  Digite `-main.css`.  O DevTools filtra `main.css` .  Se qualquer arquivo corresponde ao padrão, o tit também é filtrado.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Um filtro negativo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Um filtro negativo  
    :::image-end:::  
    
1.  Digite `domain:cdn.glitch.com` na caixa de **texto** Filtrar.  O DevTools filtra qualquer recurso com uma URL que não corresponder a esse domínio.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Um filtro de propriedade" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Um filtro de propriedade  
    :::image-end:::  
    
    Para a lista completa de propriedades filtáveis, navegue até [Filter requests by properties][DevtoolsReferenceProperty].  
    
1.  **Desempacar a** caixa de texto Filtrar de qualquer texto.  
    
### <a name="filter-by-resource-type"></a>Filtrar por tipo de recurso  

Para se concentrar em um determinado tipo de arquivo, como folhas de estilo:  

1.  Escolha **CSS**.  Todos os outros tipos de arquivo são filtrados.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Mostrar somente arquivos CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Mostrar somente arquivos CSS  
    :::image-end:::  
    
1.  Para também exibir scripts, selecione e segure `Control` \(Windows, Linux\) `Command` ou \(macOS\) e escolha **JS**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Mostrar somente arquivos CSS e JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Mostrar somente arquivos CSS e JS  
    :::image-end:::  
    
1.  Para remover os filtros e exibir todos os recursos novamente, escolha **Todos**.  
    
Para outros fluxos de trabalho de filtragem, navegue até [Solicitações de filtro][DevtoolsNetworkReferenceFilter].  

## <a name="block-requests"></a>Bloquear solicitações  

Como uma página fica e se comporta quando alguns dos recursos da página não estão disponíveis?  Falha completamente ou ainda é um pouco funcional?  Bloquear solicitações para descobrir:  

1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="O Menu De comando" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       O **Menu De comando**  
    :::image-end:::  
    
1.  Digite `block` , escolha Mostrar Bloqueio de **Solicitação**e `Enter` selecione .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Mostrar Bloqueio de Solicitação" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Mostrar Bloqueio de Solicitação**  
    :::image-end:::  
    
1.  Escolha **Adicionar Padrão** \( Adicionar Padrão ![ ](../media/add-icon.msft.png) \).  
1.  Digite `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Bloqueando main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Bloqueio `main.css`  
    :::image-end:::  
    
1.  Escolha **Adicionar**.  
1.  Atualize a página.  Como esperado, o estilo da página está um pouco confuso porque a folha de estilos principal foi bloqueada.  
    
    > [!NOTE]
    > A `main.css` linha no Log de Rede.  O texto vermelho significa que o recurso foi bloqueado.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css foi bloqueado" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` foi bloqueado  
    :::image-end:::  
    
1.  Desmarque a caixa de seleção **Habilitar bloqueio de** solicitação.  

## <a name="conclusion"></a>Conclusão  

Parabéns, você concluiu o tutorial.  Agora você sabe como usar a **ferramenta Rede** no Microsoft Edge DevTools!

Navegue até [a Referência de Rede][DevtoolsNetworkReference] para descobrir mais recursos do DevTools relacionados à inspeção da atividade de rede.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReference]: ./reference.md "Referência de análise de rede | Microsoft Docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Solicitações de filtro - Referência de análise de rede | Microsoft Docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ocultar o painel Visão geral - Referência de análise de rede | Microsoft Docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrar solicitações por propriedades - Referência de análise de rede | Microsoft Docs"
[DevToolsOpen]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com o Microsoft Edge DevTools | Microsoft Docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspecionar a demonstração de atividade de rede | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Armazenamento em cache HTTP | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/network/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
