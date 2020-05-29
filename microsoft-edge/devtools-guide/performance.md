---
description: Usar o painel desempenho para analisar a responsivenes da página durante a interação do usuário
title: DevTools-desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, desempenho, perfil, taxa de quadros, FPS, utilização da CPU, execução de JavaScript
ms.custom: seodec18
ms.openlocfilehash: aecf3cf49592dbf1f24231e76f14ddc2ca1228c3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561408"
---
# Desempenho

O painel **desempenho** oferece ferramentas para o profiling e a análise da capacidade de resposta da interface do usuário durante o curso da interação do usuário. Com ele, você pode:

 - [Medir o tempo de execução](#recording-a-profile) dos vários componentes da página 
 - Faça [Drill down para onde você está gastando mais ciclos de CPU](#timeline-ruler) para executar sua página e o efeito visual resultante para seus usuários
 - [Obter uma divisão passo a passo do tempo de execução da página de processos que](#timeline-details) está demorando 
 - [Conduza suas pilhas de chamadas JavaScript](#javascript-call-stacks) para identificar operações caras, como aquelas que exigem recálculos de layout 

![Painel de desempenho do DevTools](./media/performance.png)

## Gravando um perfil

A primeira etapa para analisar o desempenho da sua página é capturar um perfil enquanto você executa um cenário de usuário específico, como as etapas de reprodução de um bug de desempenho que você está tentando corrigir ou um caso de uso típico que você deseja otimizar para melhorar a experiência do usuário. 

### Barra de ferramentas

Use os botões **Iniciar**  /  **parar** na barra de ferramentas (ou `Ctrl+E` ) para iniciar e concluir o rastreamento de desempenho. Um indicador verde será aparecerádo na guia **desempenho** para indicar que uma gravação está em andamento. 

![Barra de ferramentas do painel desempenho](./media/performance_toolbar.png)

Um relatório de desempenho será gerado durante a interrupção do perfil. Você pode optar por salvá-lo em disco ( `Ctrl+S` ) e recarregar ( `Ctrl+O` ) no devtools mais tarde.  As sessões de diagnóstico do DevTools são salvas com a extensão *. diagsession* .

Veja algumas coisas que você precisa ter em mente ao gravar um perfil:

- Realize as ações menos necessárias para capturar o cenário que você está tentando analisar. Ações estranhas com a página produzirão dados adicionais e sobrecarregará seus resultados.

- O gerador de perfil marcará automaticamente eventos do ciclo de vida do aplicativo importante no relatório, como navegação de página, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)e [carregamento](https://developer.mozilla.org/docs/Web/Events/load)de página. Você pode adicionar marcadores personalizados chamando o método [performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) de dentro do seu código ou do console. 

- Se os tempos iniciais de carregamento da página forem importantes para a sua análise, certifique-se de limpar o cache do navegador (do painel [rede](./network.md) ) para garantir que todos os recursos da página sejam carregados da rede.

- Às vezes, ajuda a gravar várias sessões e/ou uma amostra do mesmo cenário em diferentes máquinas para compreender melhor o problema de desempenho no trabalho.

## Régua da linha do tempo

A linha do tempo funciona como uma régua deslizante. Use-o para limitar o escopo do relatório para o período de tempo específico (ou o trecho de eventos) de interesse. Arraste os **controles de slide** preto para limitar o intervalo de tempo que você deseja investigar e filtrar dados de criação de perfil incorretos dos relatórios de [linha do tempo](#timeline-details) e [pilha de chamadas de JavaScript](#javascript-call-stacks) no painel de *detalhes*inferior. 

Você verá dois tipos de marcadores na régua:

 - As **marcas do ciclo de vida do aplicativo** na linha do tempo (como navegação de página, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)e [carregamento](https://developer.mozilla.org/docs/Web/Events/load)de página) são automaticamente registradas quando você registra um perfil.

 - As **marcas do usuário** são marcadores personalizados que você pode optar por adicionar com as chamadas para o método [performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) de dentro do seu código ou do [**console**](./console.md)devtools. Você pode agrupar marcas de *início* e de *fim* juntas como uma medida nomeada única com o método [performance. Measure ()](https://developer.mozilla.org/docs/Web/API/Performance/measure) . 

Depois de selecionar um intervalo de tempo, você pode **ampliar** ainda mais a partir da barra de ferramentas ou **redefinir o zoom** e **limpar a seleção** para retornar à exibição completa do rastreamento de desempenho (sem intervalo de tempo selecionado). Esses controles também estão disponíveis no menu de contexto clique com o botão direito do mouse.

![Linha do tempo do painel de desempenho](./media/performance_timeline.png)

### Utilização da CPU

O gráfico da linha do tempo de **utilização da CPU%** descreve os recursos de processamento consumidos pelos vários subsistemas de navegador necessários para executar a página, dividida por categoria:

#### Carregando
Indica o tempo gasto na recuperação de recursos do aplicativo e a análise de HTML e CSS. Isso pode incluir solicitações de rede. Os seguintes eventos associados são registrados na [linha do tempo](#timeline-details):

Evento | Descrição
:------------ | :-------------
CssParsing  | Foi encontrado um novo conteúdo CSS que precisava ser analisado.
HtmlParsing | Foi encontrado um novo conteúdo HTML que precisava ser analisado em nós e inserido no DOM.
HttpRequest | Um recurso remoto foi encontrado no DOM ou em uma XMLHttpRequest criada que exigia uma solicitação HTTP para ser feita.
HtmlSpeculativeDownloading | O conteúdo HTML da página estava sendo pesquisado para os recursos necessários para que as solicitações HTTP para elas pudessem ser agendadas o mais rápido possível.


#### Script
Indica o tempo gasto para analisar e executar JavaScript. Isso inclui eventos DOM, temporizadores, avaliação de script e retornos de chamada de quadro de animação. Os seguintes eventos associados são registrados na [linha do tempo](#timeline-details):

Evento | Descrição
:------------ | :-------------
DomEvent | Um evento foi acionado em um objeto DOM.
EvaluatingScript | Um novo `<script>` elemento foi encontrado no dom e precisava ser analisado e executado.
EventHandler | Um ouvinte de evento registrado foi disparado em resposta a um evento DOM sendo acionado.
Quadro | Enquanto um novo quadro estava sendo preparado, um retorno de chamada registrado foi disparado para que ele pudesse contribuir com alterações visuais.
Medida | Um cenário específico do aplicativo foi medido usando o `performance.measure()` método.
MediaQueryListener | Uma consulta de mídia registrada foi invalidada, o que resultou na execução do (s) ouvinte (s) associado (s).
MutationObserver | Um ou mais elementos DOM observados foram modificados, resultando na execução de um retorno de chamada associado a um MutationObserver.
TimerFired | Um temporizador programado decorreu, resultando na execução de seu retorno de chamada associado.
WindowsRuntimeAsyncCallback | Uma operação assíncrona foi concluída por um objeto do tempo de execução do Windows que disparou um `Promise` retorno de chamada.
WindowsRuntimeEvent | Um evento foi acionado em um objeto do tempo de execução do Windows que disparou um ouvinte registrado.

#### Catálogo
Indica o tempo gasto na coleta de memória para objetos que não estão mais em uso. Os seguintes eventos associados são registrados na [linha do tempo](#timeline-details):

Evento | Descrição
:------------ | :-------------
Coleta de Lixo | O tempo de execução do JavaScript auditou o uso atual da memória do aplicativo para determinar quais objetos não estão mais sendo referenciados e, portanto, podem ser coletados.

#### Estilo
Indica o tempo gasto no cálculo da apresentação e do layout do elemento. Os seguintes eventos associados são registrados na [linha do tempo](#timeline-details):

Evento | Descrição
:------------ | :-------------
AlignedBeat | Alterações visuais pendentes feitas no DOM foram processadas para que a exibição do aplicativo pudesse ser atualizada.
CssCalculation | Foram adicionadas alterações ao DOM ou novo conteúdo CSS, exigindo que as propriedades de estilo de todos os elementos afetados sejam recalculadas.
Layout | Foram feitas alterações no DOM que exigiam que o tamanho e/ou a posição de todos os elementos afetados fossem calculados.

#### Processado
Indica o tempo gasto na pintura da tela. Os seguintes eventos associados são registrados na [linha do tempo](#timeline-details):

Evento | Descrição
:------------ | :-------------
Paint | Foram feitas alterações visuais no DOM que exigiam que todas as partes afetadas da página fossem redesenhadas.
RenderLayer | Foram feitas alterações visuais em um fragmento renderizado independentemente do DOM (chamado de uma camada) que exigia que sua respectiva parte da página fosse redesenhada.

#### Decodificação de imagem
Indica o tempo gasto para descompactar e decodificar imagens. Os seguintes eventos associados são registrados na [linha do tempo](#timeline-details):

Evento | Descrição
:------------ | :-------------
ImageDecoded | Uma imagem foi incluída no DOM e precisa ser descompactada do seu formato original para um bitmap.

### Produtividade Visual

O gráfico de **throughput Visual (FPS)** mostra os *quadros estimados por segundo* (FPS) durante o curso do cenário de perfil, em que 60 fps é a taxa de exibição ideal. DIPs na taxa de quadros indicam afunilamentos de desempenho e uma taxa de quadros igual a zero significa que os quadros estão sendo ignorados completamente.

## Detalhes do cronograma

Use o painel de detalhes último para obter a divisão completa do que aconteceu na página. A guia **detalhes da linha do tempo** fornece uma divisão de eventos que ocorreram dentro dos vários subsistemas do navegador.

![Painel de detalhes do cronograma de desempenho](./media/performance_details_timeline.png)

1. **Controle de classificação da lista de eventos**

    Use o controle suspenso **classificar por** para alternar a ordem da [lista de eventos](#event-list) entre a *hora de início* ou a *duração (inclusive*). Isso também altera o modo de exibição dos [detalhes do cronograma selecionado](#selected-timeline-details).

2. **Agrupar eventos por quadro**

    Use o botão **agrupar eventos de nível superior por quadros** para alternar entre os eventos de nível superior (*análise HTML, layout, evento DOM* etc.) na unidade de trabalho correspondente (ou "quadro") durante os períodos de tempo em que as animações/atualizações visuais estavam ocorrendo. Os quadros são tratados como outros eventos, para que possam ser classificados/filtrados e fornecer um resumo de *tempo inclusivo* quando clicados na [lista de eventos](#event-list).

3. **Controles de filtro de lista de eventos**

    Use o menu **filtrar eventos** para configurar os tipos de eventos mostrados nos [detalhes da linha do tempo](#timeline-details). 

    ![Controle para filtrar eventos de desempenho](./media/performance_filter_events.png) 

    Os seguintes filtros estão disponíveis:

   - **Decodificação de imagens**: mostrar eventos ocorridos em um thread em segundo plano (por exemplo, decodificação de imagem, GC). 
   - **Tráfego de rede**: mostrar solicitações HTTP que foram associadas à rede.
   - **Atividade da interface do usuário**: mostrar eventos ocorridos no thread da interface do usuário e/ou thread de renderização (por exemplo, manipuladores de eventos dom, layout).
   - **Medidas do usuário**: Mostre eventos personalizados que indicam chamadas para o método performance. Measure ().

     Você pode filtrar mais eventos de nível superior por sua duração inclusiva.

### Lista de eventos

A *lista de eventos* fornece uma lista cronológica de [eventos do subsistema do navegador](#cpu-utilization) que ocorreram durante o período de tempo selecionado. 

Clique em qualquer entrada para preencher o gráfico de **detalhes do evento selecionado** para esse item. As entradas com eventos/funções aninhadas mostrarão seus **inclusivos** (tempo gasto executando a função *e* quaisquer outras funções que ele chamou) e **exclusivo** (tempo gasto apenas dentro do corpo da função de chamada em si) os horários exibidos no gráfico.

Clique com o botão direito do mouse em qualquer entrada para abrir o menu de contexto para filtrar a linha do tempo somente para esse evento e exibir o código-fonte responsável pelo evento no [**depurador**](./debugger.md) (ou [**elementos**](./elements.md) , se aplicável).

### Detalhes selecionados da linha do tempo

Os *detalhes do cronograma selecionado* fornecem um gráfico de barras detalhado de tempos de evento inclusivos/exclusivos durante o intervalo de tempo selecionado. Quando você classifica por *duração (inclusive)* usando o **controle de classificação da lista de eventos**, os eventos de execução mais longos vão destacar visualmente neste gráfico. 

### Detalhes do evento selecionado

Esse relatório fornece mais informações sobre o evento selecionado, incluindo *a hora de início*, o tipo de thread em execução (por exemplo, *Download*, *interface do usuário*, *renderização*) e outros detalhes contextuais específicos do tipo de evento específico. Por exemplo, tipos de *ouvinte de eventos* fornecem links do depurador para a *função de retorno* de *chamada e agendar a pilha de chamadas*.

## Pilhas de chamadas JavaScript

![Intervalos de desempenho para pilhas de chamadas JavaScript](./media/performance_details_javascript.png)

A guia **pilhas de chamadas JavaScript** fornece informações de uso de CPU e intervalos para as funções de script executadas durante o intervalo de tempo selecionado:

 Coluna | Descrição
:------------ | :-------------
Nome da função | Nome do navegador ou função definida pelo usuário.
CPU inclusiva (%) | A porcentagem da atividade da CPU selecionada nessa função e em funções chamadas por essa função.
CPU exclusiva (%) | Porcentagem da atividade da CPU selecionada nesta função, excluindo a atividade em funções chamadas por essa função.
CPU inclusiva (MS) | Tempo de CPU gasto executando o código nesta função e em funções chamadas por esta função.
CPU exclusiva (MS) | Tempo de CPU gasto executando o código nesta função, excluindo o tempo em funções chamadas por essa função.
URL | URL (s) onde o quadro da pilha ocorreu. Chamadas de função originadas do navegador (APIs da Web baseadas em padrões) são rotuladas como *[Dom]*.

## Teclado

| Ação                         | Atalho     |
|:-------------------------------|:-------------|
| Iniciar/parar sessão de criação de perfil | `Ctrl` + `E` |
| Importar sessão de criação de perfil       | `Ctrl` + `O` |
| Exportar sessão de criação de perfil       | `Ctrl` + `S` |

## Problemas conhecidos

### Ocorreu um erro ao iniciar a sessão de criação de perfil

Se você vir esta mensagem de erro: **ocorreu um erro ao iniciar a sessão de criação de perfil** na ferramenta de desempenho, siga estas etapas para solucionar o problema.

1. Pressione `Windows Key`  +  `R` .

2. Na caixa de diálogo Executar, digite **Services. msc**.
![conhecidos-problemas-1](./media/known_issues_1.PNG)

3. Localize o **serviço coletor padrão do hub de diagnóstico da Microsoft (R)** e clique nele com o botão direito do mouse.
![conhecidos-problemas-2](./media/known_issues_2.PNG)

4. Reinicie o **serviço coletor padrão do hub de diagnóstico do Microsoft (R)**.
![conhecidos-problemas-3](./media/known_issues_3.PNG)

5. Feche as ferramentas de desenvolvedor do Microsoft Edge e a guia. Abra uma nova guia, navegue até a página e pressione `F12` .

6. Agora você deve ser capaz de começar a criação de perfil.
![conhecidos-problemas-4](./media/known_issues_4-performance.PNG)

Ainda está com problemas? Envie-nos seus comentários usando o ícone **enviar comentários** ! 

![conhecidos-problemas-5](./media/known_issues_5.PNG)

### Ocorreu um erro ao parar a sessão de criação de perfil.

Se você vir esta mensagem de erro: **ocorreu um erro ao interromper a sessão de criação de perfil** na ferramenta de desempenho, siga estas etapas para solucionar o problema.

1. Pressione `Windows Key`  +  `R` .

2. Na caixa de diálogo Executar, digite **Services. msc**.
![conhecidos-problemas-1](./media/known_issues_1.PNG)

3. Localize o **serviço coletor padrão do hub de diagnóstico da Microsoft (R)** e clique nele com o botão direito do mouse.
![conhecidos-problemas-2](./media/known_issues_2.PNG)

4. Reinicie o **serviço coletor padrão do hub de diagnóstico do Microsoft (R)**.
![conhecidos-problemas-3](./media/known_issues_3.PNG)

5. Feche as ferramentas de desenvolvedor do Microsoft Edge e a guia. Abra uma nova guia, navegue até a página e pressione `F12` .

6. Agora você deve ser capaz de começar a criação de perfil.
![conhecidos-problemas-4](./media/known_issues_4-performance.PNG)

Ainda está com problemas? Envie-nos seus comentários usando o ícone **enviar comentários** ! 

![conhecidos-problemas-5](./media/known_issues_5.PNG)
