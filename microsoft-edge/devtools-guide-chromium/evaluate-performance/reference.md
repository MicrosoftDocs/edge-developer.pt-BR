---
description: Uma referência sobre todas as maneiras de registrar e analisar o desempenho no Microsoft Edge DevTools.
title: Referência de análise de desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 181bc05fffbaef6a06bebcc5cb9ccfcc8e7de498
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398802"
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

# <a name="performance-analysis-reference"></a>Referência de análise de desempenho  

Esta página é uma referência abrangente dos recursos do Microsoft Edge DevTools relacionados à análise do desempenho.  

Navegue [até Introdução à][DevtoolsEvaluatePerformanceGettingStarted] Análise do Desempenho do Tempo de Execução para obter um tutorial guiado sobre como analisar o desempenho de uma página usando o Microsoft Edge [DevTools][MicrosoftEdgeDevTools].  

## <a name="record-performance"></a>Desempenho do registro  

### <a name="record-runtime-performance"></a>Registrar o desempenho do tempo de execução  

Grave o desempenho do tempo de execução quando quiser analisar o desempenho de uma página enquanto ela está sendo executado, em vez de carregar.  

1.  Navegue até a página que você deseja analisar.  
1.  Abra a **ferramenta Performance** no DevTools.  
1.  Escolha **Gravar** \( ![ Ícone de registro ][ImageRecordIcon] \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Interaja com a página.  O DevTools registra todas as atividades de página que ocorrem como resultado de suas interações.  
1.  Escolha **Gravar** novamente ou escolha **Parar** para interromper a gravação.  
    
### <a name="record-load-performance"></a>Registrar o desempenho da carga  

Registrar o desempenho da carga quando você quiser analisar o desempenho de uma página à medida que ela está sendo carregada, em vez de executar.  

1.  Navegue até a página que você deseja analisar.  
1.  Abra o **painel Desempenho** do DevTools.  
1.  Escolha **Atualizar página** \( Atualizar Página ![ ][ImageRefreshPageIcon] \).  O DevTools registra métricas de desempenho enquanto a página é atualizada e interrompe automaticamente a gravação alguns segundos depois que a carga é final.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Página Atualizar" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Página Atualizar**  
    :::image-end:::  
    
O DevTools amplia automaticamente a parte da gravação onde a maior parte da atividade ocorreu.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Uma gravação de carga de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Uma gravação de carga de página  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a>Capturar capturas de tela durante a gravação  

Ativar a caixa **de seleção Capturas de** Tela para capturar uma captura de tela de cada quadro durante a gravação.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="A caixa de seleção Capturas de Tela" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   A **caixa de seleção Capturas de** Tela  
:::image-end:::  

Navegue [até Exibir uma captura de](#view-a-screenshot) tela para saber como interagir com capturas de tela.  

### <a name="force-garbage-collection-while-recording"></a>Forçar a coleta de lixo durante a gravação  

Enquanto estiver gravando uma página, escolha **Coletar lixo** \( Coletar ícone de ![ lixo ][ImageCollectGarbageIcon] \) para forçar a coleta de lixo.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Coletar lixo" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Coletar lixo  
:::image-end:::  

### <a name="show-recording-settings"></a>Mostrar configurações de gravação  

Escolha **Configurações de captura** \( Configurações de captura \) para expor mais configurações relacionadas à forma como o ![ ][ImageCaptureSettingsIcon] DevTools captura gravações de desempenho.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="A seção Configurações de Captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   A **seção Configurações de** Captura  
:::image-end:::  

### <a name="disable-javascript-samples"></a>Desabilitar amostras do JavaScript  

Por padrão, a **seção Principal** de uma gravação exibe pilhas de chamadas detalhadas de funções JavaScript que foram chamadas durante a gravação.  Para desabilitar essas pilhas de chamada:  

1.  Abra o menu **Configurações de** Captura.  Navegue [até Mostrar configurações de gravação](#show-recording-settings).  
1.  Ative a caixa de seleção **Desabilitar Exemplos de JavaScript.**  
1.  Pegue uma gravação da página.  
    
As 2 figuras a seguir exibem a diferença entre desabilitar e habilenciar amostras javaScript.  A **seção Principal** da gravação é muito mais curta quando a amostragem é desabilitada, pois omite todas as pilhas de chamada JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Um exemplo de gravação quando amostras JS são desabilitadas" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Um exemplo de gravação quando amostras JS são desabilitadas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Um exemplo de uma gravação quando exemplos JS são ativas" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Um exemplo de uma gravação quando exemplos JS são ativas  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a>Acelerar a rede durante a gravação  

Para acelerar a rede durante a gravação:  

1.  Abra o menu **Configurações de** Captura.  Navegue [até Mostrar configurações de gravação](#show-recording-settings).  
1.  Definir **Rede** como o nível desejado de throttling.  
    
### <a name="throttle-the-cpu-while-recording"></a>Acelerar a CPU durante a gravação  

Para acelerar a CPU durante a gravação:  

1.  Abra o menu **Configurações de** Captura.  Navegue [até Mostrar configurações de gravação](#show-recording-settings).  
1.  Desempate a **CPU** para o nível desejado de throttling.  
    
A throttling é relativa aos recursos do computador.  Por exemplo, a opção **de lentidão 2x** faz sua CPU operar 2 vezes mais lenta do que o normal.  DevTools realmente não simulam as CPUs de dispositivos móveis, pois a arquitetura de dispositivos móveis é muito diferente da de desktops e laptops.  

### <a name="turn-on-advanced-paint-instrumentation"></a>Ativar instrumentação de tinta avançada  

Para exibir instrumentação de tinta detalhada:  

1.  Abra o menu **Configurações de** Captura.  Navegue [até Mostrar configurações de gravação](#show-recording-settings).  
1.  Marque a **caixa de seleção Habilitar instrumentação de tinta avançada (lenta).**  

Para saber como interagir com as informações de tinta, navegue até [Exibir camadas](#view-layers-information) e [Exibir profiler de tinta.](#view-paint-profiler)  

## <a name="save-a-recording"></a>Salvar uma gravação  

Para salvar uma gravação, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Salvar Perfil**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Salvar Perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Salvar Perfil**  
:::image-end:::  

## <a name="load-a-recording"></a>Carregar uma gravação  

Para carregar uma gravação, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Load Profile**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Perfil de Carga" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Perfil de Carga**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a>Limpar a gravação anterior  

Depois de fazer uma gravação, escolha **Limpar gravação** \( Limpar o ícone de gravação \) para limpar essa gravação do ![ painel ][ImageClearRecordingIcon] **Desempenho.**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Limpar gravação" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Limpar gravação**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a>Analisar uma gravação de desempenho  

Depois de [gravar o desempenho do](#record-runtime-performance) **** tempo de execução ou o desempenho da carga do [registro,](#record-load-performance)o painel Desempenho fornece muitos dados para analisar o desempenho do que acabou de acontecer.  

### <a name="select-a-portion-of-a-recording"></a>Selecione uma parte de uma gravação  

Arraste o mouse para a esquerda ou para a direita na **Visão Geral** para selecionar uma parte de uma gravação.  A **Visão** Geral é a seção que contém os **gráficos FPS,** **CPU**e **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arraste o mouse pela Visão Geral para ampliar" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Arraste o mouse pela Visão **Geral para** ampliar  
:::image-end:::  

Para selecionar uma parte usando o teclado:  

1.  Escolha o plano de fundo da seção **Principal** ou qualquer uma das seções ao lado dela, como **Interações,** **Rede**ou **GPU**.  Esse fluxo de trabalho de teclado só funciona quando uma dessas seções está em foco.  
1.  Use as teclas , , para ampliar, mover para a esquerda, diminuir o zoom e `W` mover para a `A` `S` `D` direita, respectivamente.  

Para selecionar uma parte usando um trackpad, conclua as seguintes ações.  

1.  Passe o mouse sobre a seção **Visão** Geral ou **a seção Detalhes.**  A **seção Visão** geral é a área que contém os gráficos **FPS,** **CPU**e **NET.**  A **seção Detalhes** é a área que contém a seção **Principal,** a **seção Interações** e assim por diante.  
1.  Usando dois dedos, passe o dedo para cima para diminuir o zoom, passe o dedo para a esquerda para mover para a esquerda, deslize para baixo para ampliar e passe o dedo para a direita para mover para a direita.  

Para rolar um gráfico de chama longo na **seção Principal** ou qualquer um dos vizinhos, escolha e segure enquanto arrasta para cima e para baixo.  Arraste para a esquerda e para a direita para mover qual parte da gravação foi escolhida.  

### <a name="search-activities"></a>Atividades de pesquisa  

Selecione `Control` + `F` \(Windows, Linux\) ou `Command` + `F` \(macOS\) **** para abrir a caixa de pesquisa na parte inferior do painel Desempenho.  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="A caixa de pesquisa" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   A caixa de pesquisa  
:::image-end:::  

Para navegar em atividades que corresponderem à sua consulta:  

*   Use os **botões Anterior** \( ![ Previous ][ImagePreviousIcon] \) e **Next** \( ![ Next ][ImageNextIcon] \) .  
*   Selecione `Shift` + `Enter` para selecionar o anterior ou `Enter` para selecionar o próximo.  

Para modificar as configurações de consulta:  

*   Escolha **Case sensitive** \( Case sensitive ![ ][ImageSearchCaseIcon] \) to make the query case sensitive.  
*   Escolha **Regex** \( ![ Regex ][ImageSearchRegexIcon] \) para usar uma expressão regular em sua consulta.  

Para ocultar a caixa de pesquisa, escolha **Cancelar**.  

### <a name="view-main-thread-activity"></a>Exibir atividade de thread principal  

Use a **seção Principal** para exibir a atividade que ocorreu no thread principal da página.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="A seção Principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   A **seção** Principal  
:::image-end:::  

Escolha um evento para exibir mais informações sobre ele no painel **Resumo.**  DevTools descreve o evento selecionado.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Mais informações sobre a função anônima no painel Resumo" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Mais informações sobre a `anonymous` função no painel **Resumo**  
:::image-end:::  

DevTools representa a atividade de thread principal com um gráfico de chama.  O eixo x representa a gravação ao longo do tempo.  O eixo y representa a pilha de chamada.  Os eventos na parte superior causam os eventos abaixo dele.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Um gráfico de chama" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Um gráfico de chama  
:::image-end:::  

Na figura anterior, um `click` evento causou um in na linha `Function Call` `activitytabs.js` 53.  Abaixo `Function Call` , revise se uma função anônima foi executado.  A função anônima solicitada `a` , que solicitou , que solicitou `wait` `Minor GC` .  

O DevTools atribui cores aleatórias a scripts.  Na figura anterior, as solicitações de função de um script são coloridas em verde claro.  As solicitações de outro script são bege coloridas.  O amarelo mais escuro representa a atividade de script e o evento roxo representa a atividade de renderização.  Esses eventos amarelos e roxos mais escuros são consistentes em todas as gravações.  

Navegue [até Desabilitar amostras do JavaScript](#disable-javascript-samples) se quiser ocultar o gráfico de chama detalhado das solicitações JavaScript.  Quando exemplos JS são desabilitados, somente eventos de alto nível, como `Event: choose` e da figura anterior `Function Call` `str` exibida.  

### <a name="view-activities-in-a-table"></a>Exibir atividades em uma tabela  

Depois de gravar uma página, você não precisa depender apenas da **seção Principal** para analisar atividades.  O DevTools também fornece três exibições tabular para analisar atividades.  Cada modo de exibição oferece uma perspectiva diferente sobre as atividades:  

*   Quando quiser exibir as atividades raiz que causam mais trabalho, use o painel [Árvore de](#the-call-tree-panel) Chamada.  
*   Quando você quiser exibir as atividades em que a maior parte do tempo foi gasto diretamente, use o [painel Bottom-Up.](#the-bottom-up-panel)  
*   Quando quiser exibir as atividades na ordem em que ocorreram durante a gravação, use o painel [Log de](#the-event-log-panel) Eventos.  
    
> [!NOTE]
> As próximas três seções referem-se à mesma demonstração.  Execute a demonstração por conta própria [na Demonstração de Guias de Atividade][ActivityTabsDemo].  

#### <a name="root-activities"></a>Atividades raiz  

Aqui está uma explicação do **conceito** de **** atividades raiz mencionado no painel Árvore de Chamada, painel **Bottom-Up** e Painel **de Log de** Eventos.  

As atividades raiz são aquelas que fazem com que o navegador faça algum trabalho.  Por exemplo, quando você escolhe uma página da Web, o navegador executa uma `Event` atividade como a atividade raiz.  Isso `Event` pode fazer com que um manipulador seja executado e assim por diante.  

No gráfico de chama da **seção Principal,** as atividades raiz estão na parte superior do gráfico.  Nos **painéis Árvore de Chamada** e **Log** de Eventos, as atividades raiz são os itens de nível superior.  

Navegue até o [painel Árvore de](#the-call-tree-panel) Chamada para um exemplo de atividades raiz.  

#### <a name="the-call-tree-panel"></a>O painel Árvore de Chamada  

Use o **painel Árvore de** Chamada para exibir quais atividades [raiz](#root-activities) causam mais trabalho.  

O **painel Árvore de** Chamada exibe apenas atividades durante a parte selecionada da gravação.  Navegue [até Selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para saber como selecionar partes.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="O painel Árvore de Chamada" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   O **painel Árvore de** Chamada  
:::image-end:::  

Na figura anterior, o nível superior de itens na coluna **Atividade,** como `Evaluate Script` e são atividades `Parse HTML` raiz.  O aninhamento representa a pilha de chamada.  Por exemplo, na figura anterior, `Parse HTML` que causou a causa e `Evaluate Script` `Compile Script` `(anonymous)` .  

**Self Time** representa o tempo gasto diretamente nessa atividade.  **Tempo Total** representa o tempo gasto nessa atividade ou qualquer um dos filhos.  

Escolha **Tempo Próprio**, Tempo **Total**ou **Atividade** para classificar a tabela por essa coluna.  

Use a **caixa de texto** Filtrar para filtrar eventos pelo nome da atividade.  

Por padrão, o menu **Agrupar** é definido como **Sem Agrupar**.  Use o menu **Agrupar** para classificar a tabela de atividades com base em vários critérios.  

Escolha **Mostrar Pilha Mais Pesada** \( Mostrar Pilha Mais Pesada \) para revelar outra tabela à direita da tabela ![ ][ImageShowHeaviestStackIcon] **Atividade.**  Escolha uma atividade para preencher a tabela **Pilha Mais** Pesada.  A **tabela Pilha mais pesada** exibe quais filhos da atividade selecionada levaram mais tempo para ser executado.  

#### <a name="the-bottom-up-panel"></a>O Bottom-Up painel  

Use o **painel Bottom-Up** para exibir quais atividades assumiram a maior parte do tempo agregado.  

O **painel Bottom-Up** exibe apenas atividades durante a parte selecionada da gravação.  Navegue [até Selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para saber como selecionar partes.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="O Bottom-Up painel" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   O **painel Bottom-Up**  
:::image-end:::  

No gráfico **de** chama da seção Principal da figura anterior, navegue até que praticamente todo o tempo foi gasto em `Parse HTML` execução.  A atividade superior no **painel Bottom-Up** da figura anterior é `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Navegue até **o painel Bottom-Up,** a próxima atividade mais cara é `Layout` .  

A **coluna Tempo Próprio** representa o tempo agregado gasto diretamente nessa atividade, em todas as ocorrências.  

A **coluna Tempo Total** representa o tempo agregado gasto nessa atividade ou qualquer um dos filhos.  

#### <a name="the-event-log-panel"></a>O painel Log de Eventos  

Use o **painel Log** de Eventos para exibir atividades na ordem em que ocorreram durante a gravação.  

O **painel Log** de Eventos exibe apenas atividades durante a parte selecionada da gravação.  Navegue [até Selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para saber como selecionar partes.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="O painel Log de Eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   O **painel Log de** Eventos  
:::image-end:::  

A **coluna Hora de** Início representa o ponto no qual essa atividade foi iniciada, em relação ao início da gravação.  Por exemplo, a hora de início do item selecionado na figura anterior significa que a atividade começou `175.7 ms` 175,7 ms depois que a gravação começou.  

A **coluna Tempo Próprio** representa o tempo gasto diretamente nessa atividade.  

As **colunas Tempo** Total representam o tempo gasto diretamente nessa atividade ou em qualquer um dos filhos.  

Escolha **Hora de Início,** **Hora De Auto**ou Tempo **Total** para classificar a tabela por essa coluna.

Use a **caixa de texto** Filtrar para filtrar atividades pelo nome.  

Use o menu **Duração** para filtrar todas as atividades que levaram menos de 1 ms ou 15 ms.  Por padrão, o menu **Duração** é definido como **Todos**, o que significa que todas as atividades são mostradas.  

Desabilite **as caixas de**seleção **** Carregando, **Script,** **Renderização**ou Pintura para filtrar todas as atividades dessas categorias.  

### <a name="view-gpu-activity"></a>Exibir atividade de GPU  

Exibir atividade de GPU na **seção GPU.**  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="A seção GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   A **seção GPU**  
:::image-end:::  

### <a name="view-raster-activity"></a>Exibir atividade de rasteridade  

Exibir atividade de rasteridade na **seção Raster.**  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="A seção Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   A **seção Raster**  
:::image-end:::  

### <a name="view-interactions"></a>Exibir interações  

Use a **seção Interações** para encontrar e analisar interações do usuário que aconteceram durante a gravação.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="A seção Interações" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   A **seção Interações**  
:::image-end:::  

Uma linha vermelha na parte inferior de uma interação representa o tempo gasto à espera do thread principal.  

Escolha uma interação para exibir mais informações sobre ele no painel **Resumo.**  

### <a name="analyze-frames-per-second-fps"></a>Analisar quadros por segundo (FPS)  

O DevTools fornece várias maneiras de analisar quadros por segundo:  

*   Use [o gráfico FPS para](#the-fps-chart) obter uma visão geral do FPS durante a gravação.  
*   Use [a seção Quadros](#the-frames-section) para exibir quanto tempo um quadro específico levou.  
*   Use o **medidor FPS** para uma estimativa em tempo real do FPS à medida que a página é executado.  Navegue [até Exibir quadros por segundo em tempo real com o medidor FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).  
    
#### <a name="the-fps-chart"></a>O gráfico FPS  

O **gráfico FPS** fornece uma visão geral da taxa de quadros durante a duração de uma gravação.  Em geral, quanto maior for a barra verde, melhor será a taxa de quadros.  

Uma barra vermelha acima do gráfico **FPS** é um aviso de que a taxa de quadros caiu tão baixo que provavelmente prejudicava a experiência do usuário.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="O gráfico FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   O **gráfico FPS**  
:::image-end:::  

#### <a name="the-frames-section"></a>A seção Quadros  

A **seção Quadros** informa exatamente quanto tempo um quadro específico levou.  

Passe o mouse em um quadro para exibir uma dica de ferramenta com mais informações sobre ele.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Passar o mouse em um quadro" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Passar o mouse em um quadro  
:::image-end:::  

Escolha um quadro para exibir mais informações sobre o quadro no painel **Resumo.**  DevTools descreve o quadro selecionado em azul.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Exibir um quadro no painel Resumo" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Exibir um quadro no painel **Resumo**  
:::image-end:::  

### <a name="view-network-requests"></a>Exibir solicitações de rede  

Expanda **a seção Rede** para exibir uma cascata de solicitações de rede que ocorreram durante a gravação.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="A seção Rede" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   A **seção Rede**  
:::image-end:::  

As solicitações são codificadas por cores da seguinte forma:  

*   HTML: Azul  
*   CSS: Roxo  
*   JS: Amarelo  
*   Imagens: verde  
    
Escolha uma solicitação para exibir mais informações sobre ela no painel **Resumo.**  Por exemplo, na figura **** anterior, o painel Resumo está exibindo mais informações sobre a solicitação azul selecionada na **seção** Rede.  

Um quadrado azul mais escuro na parte superior esquerda de uma solicitação significa que é uma solicitação de prioridade mais alta.  Um quadrado azul claro significa prioridade inferior.  Por exemplo, na figura anterior, a solicitação azul selecionada é de prioridade mais alta e a verde abaixo dela é de prioridade inferior.  

Na 1ª das figuras a seguir, a solicitação é representada por uma linha à esquerda, uma barra no meio com uma parte escura e uma parte clara e uma linha à `www.bing.com` direita.  No 2nd das figuras a seguir, mostra a representação correspondente da mesma solicitação no painel **Timing** da **ferramenta Rede.**  Veja como essas duas representações são mapeados umas para as outras:

*   A linha esquerda é tudo até o `Connection Start` grupo de eventos, inclusive.  Em outras palavras, é tudo antes `Request Sent` , exclusivo.  
*   A parte light da barra é `Request Sent` e `Waiting (TTFB)` .  
*   A parte escura da barra é `Content Download` .  
*   A linha direita é essencialmente o tempo gasto aguardando o thread principal.  Isso não é representado no painel **Timing.**  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="A representação de barra de linhas da solicitação www.bing.com de linha" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         A representação de barra de linhas da `www.bing.com` solicitação  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="A ferramenta Rede" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         A **ferramenta Rede**  
: ::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a>Exibir métricas de memória  

Ativar a caixa **de seleção** Memória para exibir métricas de memória da última gravação.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="A caixa de seleção Memória" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   A **caixa de seleção** Memória  
:::image-end:::  

DevTools exibe um novo gráfico **de** memória, acima do **painel Resumo.**  Também há um novo gráfico abaixo do gráfico **NET,** chamado **HEAP**.  O **gráfico HEAP** fornece as mesmas informações que a linha heap **JS** no **gráfico memória.**  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memória" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Métricas de memória  
:::image-end:::  

As linhas coloridas no mapa do gráfico para as caixas de seleção coloridas acima do gráfico.  
Desabilite uma caixa de seleção para ocultar essa categoria do gráfico.  

O gráfico exibe apenas a região da gravação que está selecionada no momento.  Por exemplo, na figura **** anterior, o gráfico Memória mostra apenas o uso da memória de cerca de 400 ms até a marca de 1750 ms.  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a>Exibir a duração de uma parte de uma gravação  

Ao analisar uma seção como **Network** ou **Main**, às vezes você precisa de uma estimativa mais precisa de quanto tempo determinados eventos demoraram.  Segure , escolha e segure e arraste para a esquerda ou para a direita `Shift` para selecionar uma parte da gravação.  Na parte inferior da sua seleção, o DevTools mostra quanto tempo essa parte demorou.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Exibir a duração de uma parte de uma gravação" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Exibir a duração de uma parte de uma gravação  
:::image-end:::  

### <a name="view-a-screenshot"></a>Exibir uma captura de tela  

Navegue [até Capturar capturas de tela durante a](#capture-screenshots-while-recording) gravação para saber como ativar capturas de tela.  

Passe o mouse na **Visão** Geral para exibir uma captura de tela de como a página era durante o momento da gravação.  A **Visão** Geral é a seção que contém os **gráficos CPU,** **FPS**e **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Exibir uma captura de tela" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Exibir uma captura de tela  
:::image-end:::  

Você também pode exibir capturas de tela escolhendo um quadro na **seção Quadros.**  DevTools exibe uma pequena versão da captura de tela no painel **Resumo.**  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Exibir uma captura de tela no painel Resumo" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Exibir uma captura de tela no painel **Resumo**  
:::image-end:::  

Escolha a miniatura no painel **Resumo** para ampliar a captura de tela.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Zoom em uma captura de tela do painel Resumo" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Zoom em uma captura de tela do painel **Resumo**  
:::image-end:::  

### <a name="view-layers-information"></a>Exibir informações sobre camadas  

Para exibir informações de camadas avançadas sobre um quadro:  

1.  [Ativar instrumentação de tinta avançada](#turn-on-advanced-paint-instrumentation).  
1.  Escolha um quadro na **seção Quadros.**  O DevTools exibe informações sobre as camadas no novo painel **Layers,** ao lado do painel **Log de** Eventos.  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="O painel Layers" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       O **painel Layers**  
    :::image-end:::  
    
Passe o mouse em uma camada para realça-la no diagrama.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Realça uma camada" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Realça uma camada  
:::image-end:::  

Para mover o diagrama:  

*   Escolha **Modo Pan** \( Modo Pan ![ ][ImagePanModeIcon] \) para mover ao longo dos eixos X e Y.  
*   Escolha **Girar Modo** \( Modo de ![ Rotação ][ImageRotateModeIcon] \) para girar ao longo do eixo Z.  
*   Escolha **Redefinir Transformar** \( ![ Redefinir Transformar ][ImageResetTransformIcon] \) para redefinir o diagrama para a posição original.  
    
### <a name="view-paint-profiler"></a>Exibir profiler de tinta  

Para exibir informações avançadas sobre um evento de tinta:  

1.  [Ativar](#turn-on-advanced-paint-instrumentation).  
1.  Escolha um **evento Paint** na **seção** Principal.  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="O painel De perfil de tinta" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       O **painel De perfil de tinta**  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a>Analisar o desempenho da renderização com a ferramenta Rendering  

Use os recursos do painel **Renderização** para ajudar a visualizar o desempenho de renderização da sua página.  

Para abrir a **ferramenta Rendering:**  

1.  [Abra o Menu de Comando][DevToolsCommandMenu].  
1.  Comece a digitar `Rendering` e selecione `Show Rendering` .  O DevTools exibe a **ferramenta Rendering** na parte inferior da janela DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="A ferramenta Rendering" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       A **ferramenta Rendering**  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a>Exibir quadros por segundo em tempo real com o medidor FPS  

O **medidor FPS** é uma sobreposição que aparece no canto superior direito do seu viewport.  Ele fornece uma estimativa em tempo real do FPS à medida que a página é executado.  Para abrir o **medidor FPS**:  

1.  Abra a **ferramenta Rendering.**  [Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Ativar a caixa de **seleção Medidor FPS.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="O medidor FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       O **medidor FPS**  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a>Exibir eventos de pintura em tempo real com Paint Flashing  

Use Paint Flashing para obter uma exibição em tempo real de todos os eventos de tinta na página.  Sempre que uma parte da página é re-pintada, o DevTools descreve essa seção em verde.  

Para ativar o Paint Flashing, conclua as seguintes ações.  

1.  Abra a **ferramenta Rendering.**  Navegue [até Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  A caixa de seleção **Pintar Piscando.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Flashing" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Paint Flashing**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a>Exibir uma sobreposição de camadas com bordas de camada  

Use **Bordas de Camada** para exibir uma sobreposição de bordas de camada e blocos na parte superior da página.  

Para ativar Bordas de Camada, conclua as seguintes ações,  

1.  Abra a **ferramenta Rendering.**  Navegue [até Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Ativar a caixa **de seleção Bordas da** Camada.  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordas de camada" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Bordas de camada**  
    :::image-end:::  
    
Navegue até os comentários [em debug_colors.cc][ChromiumDebugColors] para saber mais sobre as codificações de cores.  

### <a name="find-scroll-performance-issues-in-realtime"></a>Encontrar problemas de desempenho de rolagem em tempo real  

Use Scrolling Performance Issues para identificar elementos da página que têm ouvintes de eventos relacionados à rolagem que podem prejudicar o desempenho da página.  
DevTools descreve os elementos potencialmente problemáticos no teal.  

Para exibir problemas de desempenho de rolagem, conclua as seguintes ações. 

1.  Abra a **ferramenta Rendering.**  Navegue [até Analisar o desempenho da renderização com a ferramenta Rendering.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  A caixa de seleção **Problemas de Desempenho** de Rolagem.  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Scrolling Performance Issues indica que objetos não restritos a exibição de camada podem prejudicar o desempenho da rolagem" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Scrolling Performance Issues** indica que objetos não restritos a exibição de camada podem prejudicar o desempenho da rolagem  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abrir o Menu de Comando - Executar comandos com o Menu de Comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Começar a analisar o desempenho do tempo de execução | Microsoft Docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demonstração de guias de atividade | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc - Pesquisa de código"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
