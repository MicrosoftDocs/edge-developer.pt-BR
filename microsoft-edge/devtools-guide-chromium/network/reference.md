---
description: Uma referência abrangente dos recursos do painel Microsoft Edge DevTools Network.
title: Referência de Análise de Rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: bdb1145e7ee8ed7865b68f9fd632c4b1a30007e9
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564830"
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
# <a name="network-analysis-reference"></a>Referência de Análise de Rede  

Descubra novas maneiras de analisar como sua página é carregada nesta referência abrangente dos recursos de análise de rede Microsoft Edge DevTools.  

## <a name="record-network-requests"></a>Registrar solicitações de rede  

Por padrão, o DevTools registra todas as solicitações de rede na ferramenta **Rede,** desde que o DevTools seja aberto.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="O painel Rede" lightbox="../media/network-network-panel.msft.png":::
   A **ferramenta Rede**  
:::image-end:::  

### <a name="stop-recording-network-requests"></a>Interromper a gravação de solicitações de rede  

Para interromper a gravação de solicitações, conclua as etapas a seguir.  

1.  Na ferramenta **Rede,** escolha **Parar de gravar log de rede** \( Pare de gravar log de rede ![ ](../media/record-on-icon.msft.png) \).  Fica cinza para indicar que o DevTools não está mais gravando solicitações.  
1.  Selecione `Control` + `E` \(Windows, Linux\) `Command` + `E` ou \(macOS\) **** enquanto a ferramenta Rede estiver em foco.  

### <a name="clear-requests"></a>Limpar solicitações  

Escolha **Limpar** \( ![ Limpar ](../media/clear-requests-icon.msft.png) \) na ferramenta **Rede** para limpar todas as solicitações da tabela Solicitações.  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="O botão Limpar" lightbox="../media/network-network-clear-button.msft.png":::
   O **botão Limpar**  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a>Salvar solicitações em cargas de página  

Para salvar solicitações em cargas de página, na **ferramenta Rede,** a caixa de seleção **Preservar log.**  O DevTools salva todas as solicitações até desabilitar **o log preserve.**  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="A caixa de seleção Preservar Log" lightbox="../media/network-network-preserve-log.msft.png":::
   A **caixa de seleção Preservar Log**  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a>Capturar capturas de tela durante o carregamento da página  

Capture capturas de tela para analisar o que é exibido para os usuários enquanto aguarda a sua página ser carregada.  

Para habilitar capturas de tela, escolha **Configurações de**rede e, na ferramenta **Rede,** ative a caixa de seleção **Captura capturas de** tela.  

Atualize a página enquanto **a ferramenta Rede** está em foco para capturar capturas de tela.  

Depois de capturar uma captura de tela, você interage com ela das seguintes maneiras.  

*   Passe o mouse em uma captura de tela para exibir o ponto no qual essa captura de tela foi capturada.  Uma linha amarela é exibida no painel **Visão** geral.  
*   Escolha a miniatura de uma tela para filtrar todas as solicitações que ocorreram após a captura de tela ter sido capturada.  
*   Clique duas vezes em uma miniatura para ampliá-la.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Passar o mouse em uma captura de tela" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Passar o mouse em uma captura de tela  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a>Alterar o comportamento de carregamento  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a>Emular um visitante pela primeira vez desabilitando o cache do navegador  

Para emular como um usuário de primeira vez experimenta seu site, a caixa de seleção **Desabilitar cache.**  O DevTools desabilita o cache do navegador.  Esse recurso emula com mais precisão a experiência de um usuário pela primeira vez, pois as solicitações são atendidas do cache do navegador em visitas repetidas.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="A caixa de seleção Desabilitar Cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   A **caixa de seleção Desabilitar Cache**  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a>Desabilitar o cache do navegador na gaveta Condições de Rede  

Se você quiser desabilitar o cache enquanto estiver trabalhando em outros painéis do DevTools, use a gaveta Condições de Rede.  

1.  Abra a **gaveta Condições de** Rede.  
1.  Ativar \(ou desativar\) a caixa **de seleção Desabilitar cache.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a>Limpar manualmente o cache do navegador  

Para limpar manualmente o cache do navegador a qualquer momento, abra o menu contextual \(clique com o botão direito do mouse\) em qualquer lugar na tabela Solicitações e escolha Limpar Cache **do Navegador**.  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Escolha Limpar Cache do Navegador" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Escolha **Limpar Cache do Navegador**  
:::image-end:::  

### <a name="emulate-offline"></a>Emular offline  

Uma nova classe de aplicativos Web, denominada [Progressive Web Apps,][DevtoolsProgressiveWebApps]funciona offline com a ajuda de funcionários **do serviço.**  Você pode achar útil simular rapidamente um dispositivo que não tenha conexão de dados ao criar esse tipo de aplicativo.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Escolha o **menu suspenso Online,** pesquise em **Predefinições**e escolha **Offline** para simular uma experiência de rede offline.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="O menu suspenso Offline" lightbox="../media/network-network-offline-dropdown.msft.png":::
   O **menu** suspenso Offline  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a>Emular conexões de rede lentas  

Emular slow 3G, Fast 3G e outras velocidades de conexão do menu suspenso **Online.**  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="O menu suspenso Throttling" lightbox="../media/network-network-throttling-menu.msft.png":::
   O **menu suspenso Throttling**  
:::image-end:::  

Você pode escolher entre predefinições diferentes, como Slow 3G ou Fast 3G.  Para adicionar suas próprias predefinições personalizadas, abra o menu Throttling e escolha **Adicionar**  >  **Personalizado**.  

O DevTools exibe um ícone de aviso ao lado da **ferramenta Rede** para lembrá-lo de que a habilitação está habilitada.  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a>Emular conexões de rede lentas da gaveta Condições de Rede  

Se você quiser acelerar a conexão de rede enquanto estiver trabalhando em outros painéis de DevTools, use a gaveta Condições de Rede.  

1.  Abra a **gaveta Condições de** Rede.  
1.  Escolha a velocidade da conexão no menu **Throttling.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a>Limpar manualmente cookies do navegador  

Para limpar manualmente cookies do navegador a qualquer momento, passe o mouse em qualquer lugar na tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Limpar Cookies do Navegador**.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Escolha Limpar Cookies do Navegador" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Escolha **Limpar Cookies do Navegador**  
:::image-end:::  

### <a name="override-the-user-agent"></a>Substituir o agente do usuário  

Para substituir manualmente o agente do usuário, use as etapas a seguir.  

1.  Abra a **gaveta Condições de** Rede.  
1.  Desativar a caixa **de seleção Selecionar** automaticamente.  
1.  Escolha uma opção de agente de usuário no menu ou insira uma personalizada na caixa de texto.  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a>Solicitações de filtro  

### <a name="filter-requests-by-properties"></a>Filtrar solicitações por propriedades  

Use a **caixa de** texto Filtrar para filtrar solicitações por propriedades, como o domínio ou o tamanho da solicitação.  

Se a caixa de texto não for exibida, o painel **Filtros** provavelmente será oculto.  
Para obter mais informações, navegue até [Ocultar o painel Filtros.](#hide-the-filters-pane)  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="A caixa de texto Filtrar" lightbox="../media/network-network-filters-textbox.msft.png":::
   A **caixa de texto** Filtrar  
:::image-end:::  

Você pode usar várias propriedades simultaneamente separando cada propriedade com um espaço.  Por exemplo, `mime-type:image/png larger-than:1K` exibe todos os PNGs maiores que 1 quilobyte.  Os filtros de várias propriedades são equivalentes às `AND` operações.  `OR` no momento, não há suporte para operações.  

A lista completa de propriedades com suporte.  

| Propriedade | Detalhes |  
|:--- | :--- |  
| `domain` | Exibe apenas recursos do domínio especificado.  Você pode usar um caractere curinga \( `*` \) para incluir vários domínios.  Por exemplo, `*.com` exibe recursos de todos os nomes de domínio que terminam em `.com` .  O DevTools preenche o menu suspenso preenchimento automático com todos os domínios encontrados. |  
| `has-response-header` | Exibe os recursos que contêm o cabeçalho de resposta HTTP especificado.  O DevTools preenche o menu suspenso de preenchimento automático com todos os headers de resposta encontrados. |  
| `is` | Use `is:running` para encontrar `WebSocket` recursos. |  
| `larger-than` | Exibe recursos maiores do que o tamanho especificado, em bytes.  Definir um valor de `1000` é equivalente à definição de um valor de `1k` . |  
| `method` | Exibe recursos que foram recuperados em um tipo de método HTTP especificado.  DevTools preenche o menu suspenso com todos os métodos HTTP encontrados. |  
| `mime-type` | Exibe recursos de um tipo MIME especificado.  DevTools preenche o menu suspenso com todos os tipos MIME encontrados. |  
| `mixed-content` | Mostrar todos os recursos de conteúdo misto \( \) ou apenas os que estão atualmente `mixed-content:all` exibidos \( `mixed-content:displayed` \). |  
| `scheme` | Exibe recursos recuperados sobre HTTP \( `scheme:http` \) ou HTTPS protegido \( `scheme:https` \). |  
| `set-cookie-domain` | Exibe recursos que têm `Set-Cookie` um header com um `Domain` atributo que corresponde ao valor especificado.  DevTools preenche o preenchimento automático com todos os domínios de cookie encontrados. |  
| `set-cookie-name` | Exibe recursos que têm `Set-Cookie` um header com um nome que corresponde ao valor especificado.  DevTools preenche o preenchimento automático com todos os nomes de cookie encontrados. |  
| `set-cookie-value` | Exibe recursos que têm `Set-Cookie` um header com um valor que corresponde ao valor especificado.  DevTools preenche o preenchimento automático com todos os valores de cookie encontrados. |  
| `status-code` | Exibe recursos que corresponderem ao código de status HTTP específico.  O DevTools preenche o menu suspenso preenchimento automático com todos os códigos de status encontrados. |  

### <a name="filter-requests-by-type"></a>Filtrar solicitações por tipo  

Para filtrar solicitações por tipo de solicitação, escolha um dos seguintes botões na **ferramenta Rede.**  

:::row:::
   :::column span="1":::
      **XHR**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **JS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **CSS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Img**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Mídia**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Fonte**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Doc**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **WS**  
   :::column-end:::
   :::column span="2":::
      WebSocket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Manifesto**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Other**  
   :::column-end:::
   :::column span="2":::
      Qualquer outro tipo não listado.  
   :::column-end:::
:::row-end:::  

Se os botões não são exibidos, o painel **Filtros** pode estar oculto.  
Para obter mais informações, navegue até [Ocultar o painel Filtros.](#hide-the-filters-pane)  

Para habilitar vários filtros de tipo simultaneamente, segure `Control` \(Windows, Linux\) `Command` ou \(macOS\) e escolha.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Use os filtros Type para exibir recursos JS, CSS e Document" lightbox="../media/network-network-type-filters.msft.png":::
   Use os filtros Type para exibir recursos JS, CSS e Document  
:::image-end:::  

### <a name="filter-requests-by-time"></a>Filtrar solicitações por tempo  

Escolha e arraste para a esquerda ou para a direita no painel **Visão** geral para exibir somente solicitações que estavam ativas durante esse período.  O filtro é inclusivo.  Qualquer solicitação que estava ativa durante o horário realçado é mostrada.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrar todas as solicitações inativas em torno de 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   Filtrar todas as solicitações inativas em torno de 300 ms  
:::image-end:::  

### <a name="hide-data-urls"></a>Ocultar URLs de dados  

[URLs de dados][MDNHTTPDataURIs] são arquivos pequenos incorporados a outros documentos.  Qualquer solicitação exibida na tabela Solicitações que começa com `data:` é uma URL de dados.  

Para ocultar as solicitações, desligue a caixa de seleção **Ocultar URLs de** dados.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Caixa de seleção Ocultar URLs de Dados" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Caixa **de seleção Ocultar URLs de** Dados  
:::image-end:::  

## <a name="sort-requests"></a>Classificar solicitações  

Por padrão, as solicitações na tabela Solicitações são ordenadas por hora de início, mas você pode classificar a tabela usando outros critérios.  

### <a name="sort-by-column"></a>Classificar por coluna  

Escolha o header de qualquer coluna na solicitação para classificar solicitações por essa coluna.  

### <a name="sort-by-activity-phase"></a>Classificar por fase de atividade  

Para alterar como o Cascata classifica solicitações, passe o mouse no header da tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\), passe o mouse em **Cascata**e escolha uma das seguintes opções.  

:::row:::
   :::column span="1":::
      **Hora de início**  
   :::column-end:::
   :::column span="2":::
      A primeira solicitação iniciada está na parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tempo de Resposta**  
   :::column-end:::
   :::column span="2":::
      A primeira solicitação que começou a baixar está na parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Hora de Término**  
   :::column-end:::
   :::column span="2":::
      A primeira solicitação concluída está na parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Duração Total**  
   :::column-end:::
   :::column span="2":::
      A solicitação com as configurações de conexão mais curtas e solicitação ou resposta está na parte superior.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Latência**  
   :::column-end:::
   :::column span="2":::
      A solicitação que esperou o menor tempo para uma resposta está na parte superior.  
   :::column-end:::
:::row-end:::  

Essas descrições pressuem que cada opção respectiva é classificada da menor para a mais longa.  Escolha o header da coluna **Cascata** para reverter a ordem.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Classificar a Cascata por duração total" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Classificar a Cascata por duração total \(A parte mais leve de cada barra é o tempo gasto esperando e a parte mais escura é o tempo gasto baixando bytes\)  
:::image-end:::  

## <a name="analyze-requests"></a>Analisar solicitações  

Desde que o DevTools seja aberto, ele registra todas as solicitações na **ferramenta Rede.**  
Use o painel Rede para analisar solicitações.  

### <a name="display-a-log-of-requests"></a>Exibir um log de solicitações  

Use a tabela Solicitações para exibir um log de todas as solicitações feitas enquanto o DevTools estiver aberto.  Para revelar mais informações sobre cada item, escolha ou passe o mouse sobre solicitações.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="A tabela Solicitações" lightbox="../media/network-network-requests-table.msft.png":::
   A tabela Solicitações  
:::image-end:::  

A tabela Solicitações exibe as seguintes colunas por padrão.  

:::row:::
   :::column span="1":::
      **Nome**  
   :::column-end:::
   :::column span="2":::
      O nome do arquivo ou um identificador do recurso.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Status**  
   :::column-end:::
   :::column span="2":::
      O código de status HTTP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Tipo**  
   :::column-end:::
   :::column span="2":::
      O tipo MIME do recurso solicitado.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Iniciador**  
   :::column-end:::
   :::column span="2":::
      Os seguintes objetos ou processos iniciam solicitações.  
      
      *   **Analisador**  O analisador HTML para Microsoft Edge.  
      *   **Redirecionamento**  Um redirecionamento HTTP.  
      *   **Script**  Uma função JavaScript.  
      *   **Outros**  Algum outro processo ou ação, como navegar até uma página usando um link ou inserir uma URL na barra de endereços.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Size**  
   :::column-end:::
   :::column span="2":::
      O tamanho combinado dos headers de resposta mais o corpo da resposta, conforme fornecido pelo servidor.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Hora**  
   :::column-end:::
   :::column span="2":::
      A duração total, desde o início da solicitação até o recebimento do byte final na resposta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Cascata](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Uma divisão visual da atividade para cada solicitação.  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a>Adicionar ou remover colunas  

Passe o mouse no header da tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\) e escolha uma opção para ocultar ou mostrar.  As opções exibidas no momento têm marcas de seleção ao lado de cada item.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Adicionar uma coluna à tabela Solicitações" lightbox="../media/network-network-requests-add-column.msft.png":::
   Adicionar uma coluna à tabela Solicitações  
:::image-end:::  

#### <a name="add-custom-columns"></a>Adicionar colunas personalizadas  

Para adicionar uma coluna personalizada à tabela Solicitações, passe o mouse no header da tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Headers**de Resposta Gerenciar Colunas de  >  **Header**.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Adicionar uma coluna personalizada à tabela Solicitações" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Adicionar uma coluna personalizada à tabela Solicitações  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a>Exibir a relação de tempo das solicitações  

Use o Cascata para exibir as relações de tempo das solicitações.  
A organização padrão do Waterfall usa a hora de início das solicitações.  
Portanto, solicitações mais distantes à esquerda iniciadas anteriormente às solicitações mais distantes à direita.  

Para revisar as diferentes maneiras de classificar o Cascata, navegue até [Classificar por fase de atividade.](#sort-by-activity-phase)  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="A coluna Cascata do painel Solicitações" lightbox="../media/network-network-requests-waterfall.msft.png":::
   A coluna Cascata do painel **Solicitações**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <a name="display-a-preview-of-a-response-body"></a>Exibir uma visualização de um corpo de resposta  

Para exibir uma visualização de um corpo de resposta, use as etapas a seguir.  

1.  Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.  
1.  Escolha o **painel Visualização.**  

A guia Visualização é mais útil para exibir imagens.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="O painel Visualização" lightbox="../media/network-network-resources-preview.msft.png":::
   O **painel Visualização**  
:::image-end:::  

### <a name="display-a-response-body"></a>Exibir um corpo de resposta  

Para exibir o corpo da resposta a uma solicitação, use as etapas a seguir.  

1.  Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.  
1.  Escolha o **painel Resposta.**  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="O painel Resposta" lightbox="../media/network-network-resources-response.msft.png":::
   O **painel Resposta**  
:::image-end:::  

### <a name="display-http-headers"></a>Exibir cabeçalhos HTTP  

Para exibir dados de cabeçalho HTTP sobre uma solicitação, use as etapas a seguir.  

1.  Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.  
1.  Escolha **o psanel de headers.**  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="O painel Headers" lightbox="../media/network-resources-headers.msft.png":::
   O **painel Headers**  
:::image-end:::  

#### <a name="display-http-header-source"></a>Exibir a origem do cabeçalho HTTP  

Por padrão, o **painel Headers** mostra nomes de header em ordem alfabética.  Para dsiplay os nomes de cabeçalho HTTP na ordem recebida, use as etapas a seguir.  

1.  Abra o **painel Headers** para a solicitação que lhe interessa.  Para obter mais informações, navegue até [Exibir cabeçalhos HTTP.](#display-http-headers)  
1.  Escolha **a origem**do exibição , ao lado da seção **Header de Solicitação** **ou Dec. de** Resposta.  

### <a name="display-query-string-parameters"></a>Exibir parâmetros de cadeia de caracteres de consulta  

Para exibir os parâmetros de cadeia de caracteres de consulta de uma URL em um formato acessível por humanos, use as etapas a seguir.  

1.  Abra o **painel Headers** para a solicitação que lhe interessa.  Para obter mais informações, navegue até [Exibir cabeçalhos HTTP.](#display-http-headers)  
1.  Navegue até **a seção Parâmetros da Cadeia de Caracteres de** Consulta.  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="A seção Parâmetros da Cadeia de Caracteres de Consulta" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   A **seção Parâmetros da Cadeia de Caracteres de** Consulta  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a>Exibir a origem dos parâmetros da cadeia de caracteres de consulta  

Para exibir a fonte do parâmetro de cadeia de caracteres de consulta de uma solicitação, use as etapas a seguir.  

1.  Navegue até a seção Parâmetros da Cadeia de Caracteres de Consulta.  Para obter mais informações, navegue até [Exibir parâmetros de cadeia de caracteres de consulta](#display-query-string-parameters).  
1.  Escolha **a fonte de exibição**.  

#### <a name="display-url-encoded-query-string-parameters"></a>Exibir parâmetros de cadeia de caracteres de consulta codificada por URL  

Para exibir parâmetros de cadeia de caracteres de consulta em um formato aceitável para humanos, mas com codificações preservadas, use as etapas a seguir.  

1.  Navegue até a seção Parâmetros da Cadeia de Caracteres de Consulta.  Para obter mais informações, navegue até [Exibir parâmetros de cadeia de caracteres de consulta](#display-query-string-parameters).  
1.  Escolha **exibir URL codificada**.  

### <a name="display-cookies"></a>Exibir cookies  

Para exibir os cookies enviados no cabeçalho HTTP de uma solicitação, use as etapas a seguir.  

1.  Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.  
1.  Escolha o **painel Cookies.**  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="O painel Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   O painel Cookies  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a>Exibir a divisão de tempo de uma solicitação  

Para exibir a divisão de tempo de uma solicitação, use as etapas a seguir.  

1.  Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.  
1.  Escolha o **painel Timing.**  

Para uma maneira mais rápida de acessar os dados, navegue até [Visualizar uma divisão de tempo.](#preview-a-timing-breakdown)  

Para obter mais informações sobre cada uma das **** fases que podem ser exibidas no painel Timing, navegue até Fases de divisão [de tempo explicadas](#timing-breakdown-phases-explained).  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="O painel Timing" lightbox="../media/network-network-resources-timing.msft.png":::
   O **painel Timing**  
:::image-end:::  

Mais informações sobre cada uma das fases.  

Para obter mais informações sobre como acessar a exibição, navegue até [Exibir divisão de tempo](#display-the-timing-breakdown-of-a-request).  

#### <a name="preview-a-timing-breakdown"></a>Visualizar uma divisão de tempo  

Para exibir uma visualização da divisão de tempo de uma solicitação, na coluna **Cascata** da tabela Solicitações, passe o mouse na entrada da solicitação.  

Para obter mais informações sobre como acessar os dados sem passar o mouse, navegue até Exibir a [divisão de tempo de uma solicitação](#display-the-timing-breakdown-of-a-request).  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Visualizar a divisão de tempo de uma solicitação" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Visualizar a divisão de tempo de uma solicitação  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a>Fases de divisão de tempo explicadas  

Mais informações sobre cada uma das fases que podem ser exibidas no painel **Timing.**  

:::row:::
   :::column span="1":::
      **Filas**  
   :::column-end:::
   :::column span="2":::
      O navegador faz filas de solicitações quando qualquer um dos seguintes são verdadeiros.  
      
      *   Solicitações de prioridade mais alta existem.  
      *   Seis conexões TCP estão abertas para a mesma origem, que é o limite.  Aplica-se somente a HTTP/1.0 e HTTP/1.1.  
      *   O navegador está alocando espaço brevemente no cache de disco.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Parado**  
   :::column-end:::
   :::column span="2":::
      A solicitação está paralisada por qualquer um dos motivos descritos em **Queueing**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **DNS Lookup**  
   :::column-end:::
   :::column span="2":::
      O navegador está resolvendo o endereço IP da solicitação.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Conexão inicial**  
   :::column-end:::
   :::column span="2":::
      O navegador estabelece uma conexão, incluindo handshakes TCP, recuperações TCP e negocia uma Camada de Soquete Seguro.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Negociação de proxy**  
   :::column-end:::
   :::column span="2":::
      O navegador está negociando a solicitação com um [servidor proxy][WikiProxyServer].  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Solicitação enviada**  
   :::column-end:::
   :::column span="2":::
      A solicitação está sendo enviada.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Preparação do ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      O navegador está iniciando o trabalhador do serviço.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Solicitar ao ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      A solicitação está sendo enviada para o trabalhador do serviço.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Aguardando \(TTFB\)**  
   :::column-end:::
   :::column span="2":::
      O navegador está aguardando o primeiro byte de uma resposta.  TTFB significa Time To First Byte.  Esse tempo inclui uma viagem de ida e volta de latência e o tempo que o servidor levou para preparar a resposta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Download de conteúdo**  
   :::column-end:::
   :::column span="2":::
      O navegador está recebendo a resposta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Receber Push**  
   :::column-end:::
   :::column span="2":::
      O navegador está recebendo dados para essa resposta por meio do HTTP/2 Server Push.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Push de leitura**  
   :::column-end:::
   :::column span="2":::
      O navegador está lendo os dados locais recebidos anteriormente.  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a>Exibir iniciadores e dependências  

Para exibir os iniciadores e dependências de uma solicitação, segure e passe o mouse sobre a `Shift` solicitação na tabela Solicitações.  Cores do DevTools: os iniciadores são mostrados em verde e as dependências são mostradas em vermelho.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Exibir os iniciadores e dependências de uma solicitação" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Exibir os iniciadores e dependências de uma solicitação  
:::image-end:::  

Quando a tabela Solicitações é ordenada cronologicamente, se você passar o mouse em uma linha, a linha anterior a ela exibirá uma solicitação verde.  A solicitação verde é o iniciador da dependência.  Se outra solicitação verde for exibida na linha antes disso, essa solicitação maior será o iniciador do iniciador.  E assim em diante.  

### <a name="display-load-events"></a>Exibir eventos de carga  

O DevTools exibe o tempo dos eventos e em `DOMContentLoaded` vários locais na ferramenta `load` **Rede.**  O `DOMContentLoaded` evento é colorido em azul e o evento é `load` vermelho.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Os locais dos eventos DOMContentLoaded e load no painel Rede" lightbox="../media/network-network-requests-load-events.msft.png":::
   Os locais dos `DOMContentLoaded` eventos e na ferramenta `load` **Rede**  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a>Exibir o número total de solicitações  

O número total de solicitações está listado no painel **Resumo,** na parte inferior da **ferramenta Rede.**  

> [!CAUTION]
> Esse número só rastreia solicitações registradas desde que o DevTools foi aberto.  Se outras solicitações ocorreram antes da abertura do DevTools, essas solicitações não são contadas.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="O número total de solicitações desde que o DevTools foi aberto" lightbox="../media/network-network-total-requests.msft.png":::
   O número total de solicitações desde que o DevTools foi aberto  
:::image-end:::  

### <a name="display-the-total-download-size"></a>Exibir o tamanho total do download  

O tamanho total de download de solicitações está listado no painel **Resumo,** na parte inferior da **ferramenta Rede.**  

> [!CAUTION]
> Esse número só rastreia solicitações registradas desde que o DevTools foi aberto.  Se outras solicitações ocorreram antes da abertura do DevTools, as solicitações anteriores não são contadas.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="O tamanho total de download de solicitações" lightbox="../media/network-network-total-download-size.msft.png":::
   O tamanho total de download de solicitações  
:::image-end:::  

Para verificar a dimensão dos recursos após o navegador descompactar cada item, navegue para exibir o tamanho não [compactado de um recurso](#display-the-uncompressed-size-of-a-resource).  

### <a name="display-the-stack-trace-that-caused-a-request"></a>Exibir o rastreamento de pilha que causou uma solicitação  

Depois que uma instrução JavaScript solicitar um recurso, passe o mouse na coluna **Iniciador** para exibir o rastreamento de pilha que antecede a solicitação.  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="O rastreamento de pilha que antecede uma solicitação de recurso" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   O rastreamento de pilha que antecede uma solicitação de recurso  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a>Exibir o tamanho não compactado de um recurso  

A tela de seleção **Usar linhas de solicitação grandes** e, em seguida, revise o valor inferior da coluna **Tamanho.**  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Um exemplo de recursos não compactados" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Um exemplo de recursos não compactados \(O tamanho compactado do arquivo enviado pela rede foi , enquanto o tamanho não `jquery-3.3.1.min.js` `29.9 KB` compactado foi `84.9 KB` \)  
:::image-end:::  

## <a name="export-requests-data"></a>Exportar dados de solicitações  

### <a name="save-all-network-requests-to-a-har-file"></a>Salvar todas as solicitações de rede em um arquivo HAR  

Para salvar todas as solicitações de rede em um arquivo HAR, conclua as etapas a seguir.  

1.  Passe o mouse em qualquer solicitação na tabela Solicitações e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Salvar como HAR com Conteúdo**.  O DevTools salva todas as solicitações que ocorreram desde que você abriu o DevTools para o arquivo HAR.  Não é possível filtrar solicitações.  Você também não é capaz de salvar uma única solicitação.  

Depois de salvar um arquivo HAR, você pode importá-lo de volta para o DevTools para análise.  Basta arrastar e soltar o arquivo HAR na tabela Solicitações.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Escolha Salvar como HAR com conteúdo" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Escolha **Salvar como HAR com conteúdo**  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a>Copiar uma ou mais solicitações para a área de transferência  

Na coluna **Nome** da tabela Solicitações, passe o mouse em uma solicitação, abra o menu contextual \(clique com o botão direito do mouse\), passe o mouse em **Copiar**e escolha uma das opções a seguir.  

| Nome | Detalhes |  
|:--- |:--- |  
| **Copiar Endereço de Link** | Copie a URL da solicitação para a área de transferência. |  
| **Copiar Resposta** | Copie o corpo da resposta para a área de transferência. |  
| **Copiar como Buscar** | &nbsp; |  
| **Copiar como cURL** | Copie a solicitação como um comando cURL. |  
| **Copiar Tudo como Busca** | &nbsp; |  
| **Copiar Tudo como cURL** | Copie todas as solicitações como uma cadeia de comandos cURL. |  
| **Copiar Tudo como HAR** | Copie todas as solicitações como dados HAR. |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Escolha Copiar Resposta" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Escolha **Copiar Resposta**  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a>Copiar json de resposta formatada para a área de transferência  

Escolha uma solicitação de rede e navegue até o painel **Headers.**  Para copiar o valor JSON de uma resposta, navegue até **Solicitar**carga , passe o mouse no conteúdo de resposta JSON, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar Valor**.  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copiar Valor no menu contextual" lightbox="../media/network-header-copy-property-value.msft.png":::
          **Copiar Valor** no menu contextual  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Microsoft Visual Studio Código com resposta formatada JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          Colar json de resposta formatada em Microsoft Visual Studio Código  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a>Copiar valores de propriedade de solicitações de rede para sua área de transferência  

Para copiar valores de propriedade de solicitações de rede para sua área de transferência, conclua as seguintes ações.  

1.  Abra o **painel Headers.**  
1.  Abra uma das seções de header a seguir.  
    *   Solicitar carga \(JSON\)  
    *   Dados do formulário  
    *   Parâmetros da cadeia de caracteres de consulta  
    *   Headers de solicitação  
    *   Headers de resposta  
1.  Abra o menu contextual \(clique com o botão direito do mouse\) > **valor copiar**.  Agora você pode colar o valor em qualquer editor para revisá-lo.  
    
## <a name="change-the-layout-of-the-network-panel"></a>Alterar o layout do painel Rede  

Você pode expandir ou fechar **** seções da interface do usuário da ferramenta de rede para focalizar informações importantes.  

### <a name="hide-the-filters-pane"></a>Ocultar o painel Filtros  

Por padrão, DevTools mostra o painel **Filtros.**  
Escolha **Filtrar** \( ![ ](../media/filter-icon.msft.png) Filtrar \) para o ocultar.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="O botão Ocultar Filtros" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   O botão Ocultar Filtros  
:::image-end:::  

### <a name="use-large-request-rows"></a>Usar linhas de solicitação grandes  

Use linhas grandes quando quiser mais espaço em branco na tabela de solicitações de rede.  Algumas colunas também fornecem um pouco mais de informações ao usar linhas grandes.  Por exemplo, o valor inferior da coluna **Tamanho** é o tamanho não compactado de uma solicitação.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Um exemplo de linhas de solicitação grandes no painel Solicitações" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Um exemplo de linhas de solicitação grandes no painel **Solicitações**  
:::image-end:::  

Para habilitar linhas grandes, ative a caixa de seleção **Usar linhas de solicitação** grandes.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Caixa de seleção Usar linhas de solicitação grandes" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Caixa **de seleção Usar linhas de solicitação** grandes  
:::image-end:::  

### <a name="hide-the-overview-pane"></a>Ocultar o painel Visão Geral  

Por padrão, o DevTools exibe o painel **Visão** geral.  Para o ocultar, desligue a caixa de seleção **Mostrar Visão** Geral.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="A caixa de seleção Mostrar Visão Geral" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   A **caixa de seleção Mostrar Visão** Geral  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Depurar aplicativos Web progressivos | Microsoft Docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URLs de dados | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy - Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/network/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
