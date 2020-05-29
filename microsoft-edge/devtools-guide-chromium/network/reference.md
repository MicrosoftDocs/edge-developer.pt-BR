---
title: Referência de análise de rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611837"
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







# Referência de análise de rede   



Descubra novas maneiras de analisar como a sua página é carregada nesta referência abrangente dos recursos de análise de rede do Microsoft Edge DevTools.  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## Gravar solicitações de rede   

Por padrão, o DevTools registra todas as solicitações de rede no painel de rede, desde que DevTools esteja aberto.  

> ##### Figura 1  
> Painel de rede  
> ![Painel de rede][ImageNetworkPanel]  

### Parar a gravação de solicitações de rede   

Para parar de gravar solicitações:  

*   Selecione **parar gravação de log de rede** ![ parar de gravar ][ImageRecordOnIcon] o log de rede no painel de **rede** .  Ele fica cinza para indicar que o DevTools não está mais gravando solicitações.  
*   Pressione `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) enquanto o painel de **rede** estiver em foco.  

### Solicitações de limpeza   

Selecione **limpar** ![ limpar ][ImageClearIcon] no painel rede para limpar todas as solicitações da tabela solicitações.  

> ##### Figura 2  
> O botão limpar  
> ![O botão limpar][ImageClearButton]  

### Salvar solicitações nas cargas de página   

Para salvar as solicitações nas cargas da página, marque a caixa de seleção **preservar registro** no painel rede.  O DevTools salva todas as solicitações até você desabilitar o **preserve log**.  

> ##### Figura 3  
> A caixa de seleção preservar registro  
> ![A caixa de seleção preservar registro][ImagePreserveLogCheckBox]  

### Capturar capturas de tela durante o carregamento da página   

Capture capturas de tela para analisar o que os usuários vêem enquanto esperam pela página para carregar.  

Para habilitar capturas de tela, selecione **configurações de rede** e escolha **capturar capturas de tela** no painel **rede** .  

Recarregue a página enquanto o painel de **rede** estiver em foco para capturar capturas de tela.  

Após a captura de uma captura de tela, você interage com ela das seguintes maneiras.  

*   Passe o mouse sobre uma captura de tela para ver o ponto em que a captura de tela foi capturada.  Uma linha amarela é exibida no painel **visão geral** .  
*   Selecione a miniatura de uma tela para filtrar todas as solicitações ocorridas após a captura da captura de tela.  
*   Clique duas vezes em uma miniatura para ampliá-la.  

> ##### Figura 4  
> Passar o mouse sobre uma captura de tela  
> ![Passar o mouse sobre uma captura de tela][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## Alterar comportamento de carregamento  

### Emular um visitante da primeira vez desabilitando o cache do navegador   

Para emular como um usuário da primeira vez experimenta o seu site, marque a caixa de seleção **desabilitar cache** .  DevTools desabilita o cache do navegador.  Isso emula com mais precisão uma experiência do usuário pela primeira vez, pois as solicitações são servidas do cache do navegador em visitas repetidas.  

> ##### Figura 5  
> A caixa de seleção desabilitar cache  
> ! [A caixa de seleção desativar cache] [ImageDisableCacheCheckBox]  

#### Desabilitar o cache do navegador da gaveta de condições da rede   

Se você quiser desabilitar o cache enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.  

1.  Abra a gaveta de **condições de rede** .  
1.  Marque ou desmarque a caixa de seleção **desativar cache** .  

<!--todo: add network condition section when available -->  

### Limpar manualmente o cache do navegador   

Para limpar manualmente o cache do navegador a qualquer momento, clique com o botão direito do mouse em qualquer lugar na tabela solicitações e selecione **Limpar cache do navegador**.  

> ##### Figura 6  
> Selecionando limpar cache do navegador  
> ! [Selecionando limpar cache do navegador] [ImageClearBrowserCache]  

### Emular offline   

Uma nova classe de aplicativos Web, chamada [Web Apps progressivos][DevtoolsProgressiveWebApps], funciona offline com a ajuda do **serviço de trabalho**.  Pode ser útil simular rapidamente um dispositivo que não tem conexão de dados quando você está criando esse tipo de aplicativo.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Selecione o menu suspenso **online** , procure em **predefinições**e selecione **offline** para simular uma experiência de rede completamente offline.  

> ##### Figura 7  
> O menu suspenso offline  
> ! [Menu suspenso offline] [ImageOfflineDropdown]  

### Emular conexões de rede lentas   

Emular a conexão 3G, rápida 3G e outras velocidades de conexão a partir do menu suspenso **online** .  

> ##### Figura 8  
> O menu suspenso limitação  
> ! [O menu suspenso limitação] [ImageNetworkThrottlingMenu]  

Você pode escolher entre uma variedade de predefinições, como 3G ou Fast 3G lento.  Você também pode adicionar suas próprias predefinições personalizadas abrindo o menu de limitação e selecionando **Custom**  >  **Adicionar**personalizado.  

O DevTools exibe um ícone de aviso ao lado da guia **rede** para lembrá-lo de que a limitação está habilitada.  

#### Emular conexões de rede lentas da gaveta de condições da rede   

Se você quiser controlar a conexão de rede enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.  

1.  Abra a gaveta de **condições de rede** .  
1.  Selecione a velocidade de conexão desejada no menu **limitação** .  

<!--todo: add network condition section when available -->  

### Limpar manualmente os cookies do navegador   

Para limpar manualmente os cookies do navegador a qualquer momento, clique com o botão direito do mouse em qualquer lugar na tabela solicitações e selecione **Limpar cookies do navegador**.  

> ##### Figura 9  
> Selecionando limpar cookies do navegador  
> ! [Selecionando limpar cookies do navegador] [ImageClearBrowserCookies]  

### Substituir o agente do usuário   

Para substituir manualmente o agente do usuário:  

1.  Abra a gaveta de **condições de rede** .  
1.  Desmarque **selecionar automaticamente**.  
1.  Escolha uma opção de agente do usuário no menu ou insira uma opção personalizada na caixa de texto.  

<!--todo: add network condition section when available -->  

## Filtrar solicitações   

### Filtrar solicitações por propriedades   

Use a caixa de texto **Filtrar** para filtrar solicitações por propriedades, como o domínio ou o tamanho da solicitação.  

Se você não vir a caixa de texto, o painel filtros provavelmente está oculto.  
Consulte [ocultar o painel filtros](#hide-the-filters-pane).  

> ##### Figura 10  
> A caixa de texto filtros  
> ! [A caixa de texto filtros] [ImageFilterTextBox]  

Você pode usar várias propriedades simultaneamente, separando cada propriedade com um espaço.  Por exemplo, `mime-type:image/png larger-than:1K` exibe todas as PNGs maiores do que um kilobyte.  Esses filtros de várias propriedades são equivalentes às `AND` operações.  `OR` Não há suporte para operações no momento.  

A lista completa de propriedades com suporte.  

| Propriedade | Detalhes |  
|:--- | :--- |  
| `domain` | Exiba somente os recursos do domínio especificado.  Você pode usar um caractere curinga \ ( `*` \) para incluir vários domínios.  Por exemplo, `*.com` exibe os recursos de todos os nomes de domínio terminam em `.com` .  DevTools preenche o menu suspenso de preenchimento automático com todos os domínios encontrados. |  
| `has-response-header` | Mostrar os recursos que contêm o cabeçalho de resposta HTTP especificado.  DevTools preenche a lista suspensa preenchimento automático com todos os cabeçalhos de resposta detectados. |  
| `is` | Use `is:running` para localizar `WebSocket` recursos. |  
| `larger-than` | Mostrar recursos maiores do que o tamanho especificado, em bytes.  Definir um valor `1000` é equivalente a definir um valor de `1k` . |  
| `method` | Mostrar recursos que foram recuperados em um tipo de método HTTP especificado.  DevTools preenche a lista suspensa com todos os métodos HTTP que ele encontrou. |  
| `mime-type` | Mostrar recursos de um tipo MIME especificado.  DevTools preenche a lista suspensa com todos os tipos de MIME encontrados. |  
| `mixed-content` | Mostrar todos os recursos de conteúdo mistos \ ( `mixed-content:all` \) ou apenas aqueles que são exibidos no momento \ ( `mixed-content:displayed` \). |  
| `scheme` | Mostrar recursos recuperados por HTTP \ ( `scheme:http` \) ou HTTPS protegido \ ( `scheme:https` \) protegido. |  
| `set-cookie-domain` | Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um `Domain` atributo que corresponde ao valor especificado.  DevTools preenche o preenchimento automático com todos os domínios de cookies que ele encontrou. |  
| `set-cookie-name` | Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um nome que corresponde ao valor especificado.  DevTools preenche o preenchimento automático com todos os nomes de cookies que ele encontrou. |  
| `set-cookie-value` | Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um valor que corresponde ao valor especificado.  DevTools preenche o preenchimento automático com todos os valores de cookies que ele encontrou. |  
| `status-code` | Mostre apenas os recursos para os quais o código de status HTTP corresponde ao código especificado.  DevTools preenche o menu suspenso preenchimento automático com todos os códigos de status encontrados. |  

### Filtrar solicitações por tipo   

Para filtrar solicitações por tipo de solicitação, selecione o **XHR**, **js**, **CSS**, **img**, **mídia**, **fonte**, **Doc**, **WS** \ (WebSocket \), **manifesto**ou **outros** \ (qualquer outro tipo não listado aqui \) botões no painel de rede.  

Se você não vir esses botões, o painel filtros provavelmente ficará oculto.  
Consulte [ocultar o painel filtros](#hide-the-filters-pane).  

Para habilitar vários filtros de tipo simultaneamente, segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e, em seguida, selecione.  

> ##### Figura 11  
> Usar os filtros de tipo para exibir os recursos de documento, CSS e JS  
> ! [Usando os filtros de tipo para exibir os recursos JS, CSS e de documento] [ImageMultiTypeFilter]  

### Filtrar solicitações por tempo   

Selecione e arraste para a esquerda ou direita no painel Visão geral para exibir apenas as solicitações que estavam ativas durante esse período de tempo.  O filtro é inclusivo.  Todas as solicitações ativas durante o tempo realçado são mostradas.  

> ##### Figura 12  
> Filtragem de todas as solicitações que estavam inativas em torno de 300ms  
> ! [Filtragem de todas as solicitações que estavam inativas em torno de 300ms] [ImageOverviewFilter]  

### Ocultar URLs de dados  

As [URLs de dados][MDNHTTPDataURIs] são pequenos arquivos incorporados a outros documentos.  Qualquer solicitação que você vê na tabela solicitações que começa com `data:` é uma URL de dados.  

Marque a caixa de seleção **ocultar URLs de dados** para ocultar essas solicitações.  

> ##### Figura 13  
> A caixa de seleção Ocultar URLs de dados  
> ! [A caixa de seleção Ocultar URLs de dados] [ImageHideDataURLsCheckBox]  

## Solicitações de classificação  

Por padrão, as solicitações na tabela solicitações são classificadas por hora de início, mas você pode classificar a tabela usando outros critérios.  

### Classificar por coluna   

Selecione o cabeçalho de qualquer coluna nas solicitações para classificar solicitações por essa coluna.  

### Fase classificar por atividade   

Para alterar a forma como a cascata classifica solicitações, clique com o botão direito do mouse no cabeçalho da tabela solicitações, passe o mouse sobre a **cascata**e selecione uma das opções a seguir.  

*   **Hora de início**.  A primeira solicitação iniciada está na parte superior.  
*   **Tempo de resposta**.  A primeira solicitação iniciada para download está na parte superior.  
*   **Hora de término**.  A primeira solicitação que terminou está na parte superior.  
*   **Duração total**.  A solicitação com a configuração de conexão mais curta e solicitação/resposta está na parte superior.  
*   **Latência**.  A solicitação que aguardou o tempo mais curto para uma resposta está na parte superior.  

Essas descrições pressupõem que cada opção respectiva seja classificada da mais curta para a mais longa.  A seleção do cabeçalho da coluna em **cascata** inverte a ordem.  

> ##### Figura 14  
> Classificar a cascata com duração total \ (a parte mais clara de cada barra é o tempo gasto aguardando e a parte mais escura é o tempo gasto para baixar bytes \)  
> ! [Classificar a cascata por duração total] [ImageWaterfallTotalDuration]  

## Analisar solicitações   

Desde que o DevTools esteja aberto, ele registra todas as solicitações no painel de rede.  
Use o painel rede para analisar solicitações.  

### Exibir um log de solicitações   

Use a tabela requests para exibir um log de todas as solicitações feitas enquanto o DevTools está aberto.  Selecionar ou passar o mouse nas solicitações revela mais informações sobre cada item.  

> ##### Figura 15  
> A tabela solicitações  
> ! [A tabela de solicitações] [ImageRequestsTable]  

A tabela solicitações exibe as seguintes colunas por padrão:  

*   **Nome**.  O nome do recurso ou um identificador para o recurso.  
*   **Status**.  O código de status HTTP.  
*   **Tipo**.  O tipo MIME do recurso solicitado.  
*   **Iniciador**.  Os seguintes objetos ou processos iniciam solicitações:  
    *   **Analisador**.  O analisador HTML para Microsoft Edge.  
    *   **Redirecionar**.  Um redirecionamento HTTP.  
    *   **Script**.  Uma função JavaScript.  
    *   **Outros**.  Algum outro processo ou ação, como navegar para uma página por meio de um link ou inserir uma URL na barra de endereços.  
*   **Tamanho**.  O tamanho combinado dos cabeçalhos de resposta mais o corpo da resposta, conforme entregue pelo servidor.  
*   **Tempo**.  A duração total, desde o início da solicitação até o recebimento do byte final na resposta.  
*   [**Cascata**](#view-the-timing-of-requests-in-relation-to-one-another).  Uma divisão Visual da atividade para cada solicitação.  

#### Adicionar ou remover colunas   

Clique com o botão direito do mouse no cabeçalho da tabela solicitações e selecione uma opção para ocultá-la ou mostrá-la.  As opções atualmente exibidas têm marcas de opção ao lado de cada item.  

> ##### Figura 16  
> Adicionar uma coluna à tabela solicitações  
> ! [Adicionando uma coluna à tabela solicitações] [ImageRequestsTableAddColumn]  

#### Adicionar colunas personalizadas   

Para adicionar uma coluna personalizada à tabela solicitações, clique com o botão direito do mouse no cabeçalho da tabela solicitações e selecione **cabeçalhos de resposta**  >  **gerenciar colunas de cabeçalho**.  

> ##### Figura 17  
> Adicionando uma coluna personalizada à tabela solicitações  
> ! [Adicionando uma coluna personalizada à tabela de solicitações] [ImageRequestsTableCustomColumn]  

### Exibir o intervalo de solicitações em relação umas as outras   

Use a cascata para ver o intervalo de solicitações em relação umas as outras.  
Por padrão, a cascata é organizada pela hora de início das solicitações.  
Portanto, as solicitações mais distantes do lado esquerdo são mais antigas do que aquelas mais distantes do lado direito.  

Consulte a [fase classificar por atividade](#sort-by-activity-phase) para ver as diferentes maneiras de classificar a cascata.  

> ##### Figura 18  
> A coluna de cascata do painel solicitações  
> ! [A coluna em cascata do painel solicitações] [ImageRequestsTableWaterfallColumn]  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### Exibir uma visualização de um corpo de resposta   

Para exibir uma visualização do corpo de uma resposta:  

1.  Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.  
1.  Selecione a guia **Visualizar** .  

Esta guia é principalmente útil para exibir imagens.  

> ##### Figura 19  
> A guia Visualização  
> ! [A guia Visualização] [ImagePreview]  

### Exibir um corpo de resposta   

Para exibir o corpo da resposta a uma solicitação:  

1.  Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.  
1.  Selecione a guia **resposta** .  

> ##### Figura 20  
> A guia resposta  
> ! [A guia resposta] [ImageResponse]  

### Exibir cabeçalhos HTTP   

Para ver os dados do cabeçalho HTTP sobre uma solicitação:  

1.  Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.  
1.  Selecione a guia **cabeçalhos** .  

> ##### Figura 21  
> A guia cabeçalhos  
> ! [A guia cabeçalhos] [ImageHeaders]  

#### Exibir fonte de cabeçalho HTTP   

Por padrão, a guia cabeçalhos mostra os nomes dos cabeçalhos em ordem alfabética.  Para exibir os nomes dos cabeçalhos HTTP na ordem em que foram recebidos:  

1.  Abra a guia **cabeçalhos** para a solicitação que lhe interessa.  Consulte [exibir cabeçalhos HTTP](#view-http-headers).  
1.  Selecione **Exibir fonte**, ao lado da seção cabeçalho da **solicitação** ou **cabeçalho de resposta** .  

### Exibir parâmetros da cadeia de caracteres de consulta   

Para exibir os parâmetros da cadeia de caracteres de consulta de uma URL em um formato legível por pessoas:  

1.  Abra a guia **cabeçalhos** para a solicitação que lhe interessa.  Consulte [exibir cabeçalhos HTTP](#view-http-headers).  
1.  Vá para a seção **parâmetros da cadeia de caracteres de consulta** .  

> ##### Figura 22  
> A seção parâmetros da cadeia de consulta  
> ! [Seção parâmetros da cadeia de consulta] [ImageQueryStringParameters]  

#### Exibir origem dos parâmetros da cadeia de consulta   

Para exibir a origem do parâmetro da cadeia de caracteres de consulta de uma solicitação:  

1.  Vá para a seção parâmetros da cadeia de caracteres de consulta.  Consulte [Exibir parâmetros da cadeia de consulta](#view-query-string-parameters).  
1.  Selecione **Exibir código-fonte**.  

#### Exibir parâmetros da cadeia de consulta codificada por URL   

Para exibir os parâmetros da cadeia de caracteres de consulta em um formato legível pelo homem, mas com codificações preservadas:  

1.  Vá para a seção parâmetros da cadeia de caracteres de consulta.  Consulte [Exibir parâmetros da cadeia de consulta](#view-query-string-parameters).  
1.  Selecione **exibir URL codificada**.  

### Exibir cookies   

Para exibir os cookies enviados no cabeçalho HTTP de uma solicitação:  

1.  Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.  
1.  Selecione a guia **cookies** .  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

> ##### Figura 23  
> A guia cookies  
> ! [A guia cookies] [ImageCookies]  

### Exibir a divisão de tempo de uma solicitação   

Para exibir a divisão de tempo de uma solicitação:  

1.  Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.  
1.  Selecione a guia **intervalo** .  

Consulte [Visualizar um detalhamento de intervalos](#preview-a-timing-breakdown) para obter uma maneira mais rápida de acessar esses dados.  

Veja as [fases da divisão de intervalo explicadas](#timing-breakdown-phases-explained) para obter mais informações sobre cada uma das fases que você pode ver na guia intervalo.  

> ##### Figura 24  
> A guia intervalo  
> ! [A guia intervalo] [ImageTiming]  

Mais informações sobre cada uma das fases.  

Consulte [Exibir detalhamento de intervalo](#view-the-timing-breakdown-of-a-request) para obter outra maneira de acessar este modo de exibição.  

#### Visualizar uma divisão de intervalo   

Para exibir uma visualização da divisão de tempo de uma solicitação, passe o mouse sobre a entrada da solicitação na coluna **cascata** da tabela solicitações.  

Consulte [Exibir o detalhamento de intervalos de uma solicitação](#view-the-timing-breakdown-of-a-request) para acessar esses dados que não exigem o foco.  

> ##### Figura 25  
> Visualizando a divisão de tempo de uma solicitação  
> ! [Visualização da divisão de tempo de uma solicitação] [ImageWaterfallHover]  

#### Fases da divisão de tempo explicadas   

Mais informações sobre cada uma das fases que você pode ver na guia intervalo:  

*   Em **fila**.  O navegador solicita uma fila quando:  
    *   Há solicitações de prioridade mais alta.  
    *   Já existem seis conexões TCP abertas para essa origem, que é o limite.  Aplica-se somente a HTTP/1.0 e HTTP/1.1.  
    *   O navegador está alocando um espaço brevemente no cache de disco.  
*   **Parado**.  A solicitação pode estar parada para qualquer um dos motivos descritos no **enfileiramento**.  
*   **Pesquisa de DNS**.  O navegador está resolvendo o endereço IP da solicitação.  
*   **Negociação de proxy**.  O navegador está negociando a solicitação com um [servidor proxy][WikiProxyServer].  
*   **Solicitação enviada**.  A solicitação está sendo enviada.  
*   **Preparação do serviço**.  O navegador está iniciando o trabalhador do serviço.  
*   **Solicitação ao serviço de serviço**.  A solicitação está sendo enviada para o trabalhador do serviço.  
*   **Aguardando \ (TTFB \)**.  O navegador está aguardando o primeiro byte de uma resposta.  
  TTFB significa tempo até o primeiro byte.  Esse tempo inclui 1 viagem de ida e volta da latência e o tempo que o servidor levou para preparar a resposta.  
*   **Download de conteúdo**.  O navegador está recebendo a resposta.  
*   **Recebendo Push**.  O navegador está recebendo dados para esta resposta via Push HTTP/2 Server Push.  
*   **Leitura por push**.  O navegador está lendo os dados locais anteriormente recebidos.  

### Exibir iniciadores e dependências   

Para ver os iniciadores e as dependências de uma solicitação, mantenha o `Shift` cursor sobre a solicitação na tabela solicitações.  Cores DevTools: os iniciadores são exibidos em verde e as dependências são mostradas em vermelho.  

> ##### Figura 26  
> Exibindo os iniciadores e as dependências de uma solicitação  
> ! [Exibindo os iniciadores e as dependências de uma solicitação] [ImageRequestInitiatorsDependencies]  

Quando a tabela de solicitações é ordenada cronologicamente, a primeira solicitação verde acima da que você está passando é o iniciador da dependência.  Se outra solicitação verde aparecer acima disso, essa solicitação mais alta será o iniciador do iniciador.  E assim em diante.  

### Exibir eventos de carga   

DevTools exibe a temporização dos `DOMContentLoaded` eventos e de `load` vários locais no painel de rede.  O `DOMContentLoaded` evento está em azul colorido e o `load` evento está em vermelho.  

> ##### Figura 27  
> Os locais dos `DOMContentLoaded` eventos e do `load` painel de rede  
> ! [Os locais dos eventos DOMContentLoaded e Load no painel de rede] [ImageNetworkPanelDOMContentLoadedLoadEvents]  

### Ver o número total de solicitações   

O número total de solicitações está listado no painel Resumo, na parte inferior do painel de rede.  

> [!CAUTION]
> Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.  Se ocorrerem outras solicitações antes da abertura do DevTools, essas solicitações não serão contadas.  

> ##### Figura 28  
> O número total de solicitações desde que o DevTools foi aberto  
> ! [O número total de solicitações desde que o DevTools foi aberto] [ImageTotalRequests]  

### Ver o tamanho total do download   

O tamanho total do download de solicitações é listado no painel Resumo, na parte inferior do painel de rede.  

> [!CAUTION]
> Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.  Se ocorrerem outras solicitações antes da abertura do DevTools, essas solicitações não serão contadas.  

> ##### Figura 29  
> O tamanho total do download de solicitações  
> ! [O tamanho total do download de solicitações] [ImageTotalSize]  

Consulte [Exibir o tamanho descompactado de um recurso](#view-the-uncompressed-size-of-a-resource) para ver a quantidade de recursos grandes após o navegador descompactar cada item.  

### Exibir o rastreamento de pilha que causou uma solicitação   

Depois que uma instrução JavaScript solicita um recurso, passe o mouse sobre a coluna do **iniciador** para exibir o rastreamento de pilha que leva à solicitação.  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

> ##### Figura 30  
> O rastreamento de pilha que leva a uma solicitação de recurso  
> ! [O rastreamento de pilha que leva à solicitação de recurso] [ImageInitiatorStack]  

### Exibir o tamanho descompactado de um recurso   

Marque a caixa de seleção **usar linhas de solicitação grandes** e examine o valor inferior da coluna **tamanho** .  

> ##### Figura 31  
> Um exemplo de recursos não compactados \ (o tamanho compactado do `jquery-3.3.1.min.js` arquivo que foi enviado pela rede foi `29.9 KB` , enquanto o tamanho não compactado era `84.9 KB` \)  
> ! [Um exemplo de recursos não compactados] [ImageUncompressedResources]  

## Exportar dados de solicitações   

### Salvar todas as solicitações de rede em um arquivo HAR   

Para salvar todas as solicitações de rede em um arquivo HAR:  

1.  Clique com o botão direito do mouse em qualquer solicitação na tabela solicitações.  
1.  Selecione **salvar como Har com conteúdo**.  DevTools salva todas as solicitações ocorridas desde que você abriu o DevTools para o arquivo HAR.  Não há nenhuma maneira de filtrar solicitações ou salvar uma única solicitação.  

Depois de salvar um arquivo HAR, você poderá importá-lo novamente no DevTools para análise.  Basta arrastar e soltar o arquivo HAR na tabela solicitações.  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### Figura 32  
> Selecionando salvar como HAR com conteúdo  
> ! [Selecionando salvar como HAR com conteúdo] [ImageSaveAsHAR]  

### Copiar uma ou mais solicitações para a área de transferência   

Na coluna **nome** da tabela solicitações, clique com o botão direito do mouse em uma solicitação, passe o mouse sobre a **cópia**e selecione uma das seguintes opções:  

*   **Copie o endereço do link**.  Copie a URL da solicitação para a área de transferência.  
*   **Copiar resposta**.  Copie o corpo da resposta para a área de transferência.  
*   **Copiar como busca**.  
*   **Copiar como ondulação**.  Copie a solicitação como um comando de rotação.  
*   **Copiar tudo como busca**.  
*   **Copiar tudo como ondulado**.  Copie todas as solicitações como uma cadeia de comandos de ondulação.  
*   **Copiar tudo como Har**.  Copie todas as solicitações como dados de HAR.  

> ##### Figura 33  
> Selecionando a resposta de cópia  
> ! [Selecionando resposta de cópia] [ImageCopyResponse]  

## Alterar o layout do painel de rede  

Você pode expandir ou recolher seções da interface do usuário do painel de rede para concentrar informações importantes.  

### Ocultar o painel filtros   

Por padrão, o DevTools mostra o **painel filtros**.  
Selecione **Filter** ![ filtro ][ImageFilterIcon] de filtro para ocultá-lo.  

> ##### Figura 34  
> O botão Ocultar filtros  
> ! [O botão Ocultar filtros] [ImageHideFiltersButton]  

### Usar linhas de solicitação grandes   

Use linhas grandes quando quiser mais espaço em branco na tabela solicitações de rede.  Algumas colunas também fornecem um pouco mais de informações ao usar linhas grandes.  Por exemplo, o valor inferior da coluna **tamanho** é o tamanho descompactado de uma solicitação.  

> ##### Figura 35  
> Um exemplo de linhas de solicitação grandes no painel solicitações  
> ! [Um exemplo de linhas de solicitação grandes no painel solicitações] [ImageLargeRequestRows]  

Marque a caixa de seleção **usar linhas de solicitação grandes** para habilitar linhas grandes.  

> ##### Figura 36  
> A caixa de seleção de linhas de solicitação grandes  
> ! [A caixa de seleção solicitar linhas grandes] [ImageLargeRequestRowsCheckbox]  

### Ocultar o painel Visão geral   

Por padrão, o DevTools mostra o **painel Visão geral**.  
Desmarque a caixa de seleção **Mostrar visão geral** para ocultá-la.  

> ##### Figura 37  
> A caixa de seleção Mostrar visão geral  
> ! [A caixa de seleção Mostrar visão geral] [ImageHideOverviewCheckbox]  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Figura 1: painel de rede"  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Figura 2: o botão limpar"  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Figura 3: caixa de seleção preservar registro"  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Figura 4: passando o mouse sobre uma captura de tela"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Disable-cache-CheckBox.msft.png "Figura 5: a caixa de seleção desativar cache"  
[ImageClearBrowserCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-browser-cache.msft.png "Figura 6: selecionando limpar cache do navegador"  
[ImageOfflineDropdown]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-offline-DropDown.msft.png "Figura 7: o menu suspenso offline"  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-throttling-menu.msft.png "Figura 8: o menu de limitação de rede"  
[ImageClearBrowserCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-browser-cookies.msft.png "Figura 9: selecionando limpar cookies do navegador"  
[ImageFilterTextBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Filters-TextBox.msft.png "Figura 10: a caixa de texto filtros"  
[ImageMultiTypeFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Type-Filters.msft.png "Figura 11: usar os filtros de tipo para exibir os recursos de JS, CSS e documentos"  
[ImageOverviewFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Overview-Filter.msft.png "Figura 12: filtrar todas as solicitações que estavam inativas em torno de 300ms"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Hide-data-URLs.msft.png "Figura 13: caixa de seleção Ocultar URLs de dados"  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Waterfall-total-duration.msft.png "Figura 14: classificando a cascata por duração total"  
[ImageRequestsTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Table.msft.png "Figura 15: a tabela de solicitações"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Column.msft.png "Figura 16: adicionando uma coluna à tabela de solicitações"  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Custom.msft.png "figura 17: adicionando uma coluna personalizada à tabela de solicitações"  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Waterfall.msft.png "Figura 18: a coluna de cascata do painel solicitações"  
[ImagePreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Preview.msft.png "Figura 19: a guia Visualizar"  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[ImageResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Response.msft.png "Figura 20: a guia resposta"  
[ImageHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Resources-Headers.msft.png "figura 21: a guia cabeçalhos"  
[ImageQueryStringParameters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Headers-Query-String-Parameters.msft.png "Figura 22: seção de parâmetros da cadeia de consulta"  
[ImageCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-cookies.msft.png "Figura 23: a guia cookies"  
[ImageTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-timing.msft.png "Figura 24: a guia intervalo"  
[ImageWaterfallHover]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-hover.msft.png "figura 25: visualizando a divisão de tempo de uma solicitação"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-initiators-Dependencies.msft.png "Figura 26: exibindo os iniciadores e as dependências de uma solicitação"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Load-Events.msft.png "Figura 27: os locais dos eventos DOMContentLoaded e Load no painel de rede"  
[ImageTotalRequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-requests.msft.png "Figura 28: o número total de solicitações desde que o DevTools foi aberto"  
[ImageTotalSize]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-download-size.msft.png "figura 29: o tamanho total do download de solicitações"  
[ImageInitiatorStack]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Initiator-Stack.msft.png "figura 30: o rastreamento de pilha que leva até uma solicitação de recurso"  
[ImageUncompressedResources]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-uncompressed-Compare.msft.png "figura 31: um exemplo de recursos não compactados"  
[ImageSaveAsHAR]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Save-Har-Content.msft.png "Figura 32: selecionando salvar como HAR com conteúdo"  
[ImageCopyResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Copy-Response.msft.png "figura 33: selecionando cópia de resposta"  
[ImageHideFiltersButton]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Hide-Filters-Button.msft.png "Figura 34: o botão Ocultar filtros"  
[ImageLargeRequestRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Large-Request-Rows.msft.png "Figura 35: um exemplo de linhas de solicitação grandes no painel solicitações"  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-use-Large-Request-Rows-on.msft.png "Figura 36: a caixa de seleção de linhas de solicitação grandes"  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-show-Overview-off.msft.png "figura 37: a caixa de seleção Ocultar visão geral"  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Depurar aplicativos Web progressivos"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URLs de dados | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
