---
title: Referência de análise de desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611745"
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







# Referência de análise de desempenho   



Esta página é uma referência abrangente do Microsoft Edge DevTools recursos relacionados à análise de desempenho.  

Consulte [introdução ao analisando o desempenho do tempo de execução][DevtoolsEvaluatePerformanceGettingStarted] para obter um tutorial guia sobre como analisar o desempenho de uma página usando [o Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Desempenho do registro   

### Desempenho do registro em tempo de execução   

Grave o desempenho do tempo de execução quando quiser analisar o desempenho de uma página enquanto ela estiver em execução, em oposição a carregá-la.  

1.  Vá para a página que você deseja analisar.  
1.  Clique na guia **desempenho** do devtools.  
1.  Clique em **gravar** ![ registro ][ImageRecordIcon] .  
    
    > ##### Figura 1  
    > **Record**  
    > ![Record][ImageRecord]  

1.  Interagir com a página.  O DevTools registra todas as atividades de página que ocorrem como resultado de suas interações.  
1.  Clique em **gravar** novamente ou em **parar** para parar a gravação.  

### Desempenho da carga de registros   

Grave o desempenho de carga quando quiser analisar o desempenho de uma página enquanto ela estiver sendo carregada, em vez de executá-la.  

1.  Vá para a página que você deseja analisar.  
1.  Abra o painel **desempenho** do devtools.  
1.  Clique em atualizar página de atualização de **página** ![ ][ImageRefreshPageIcon] .  O DevTools registra métricas de desempenho enquanto a página é atualizada e, em seguida, interrompe automaticamente a gravação em alguns segundos após o término da carga.  
    
    > ##### Figura 2  
    > **Atualizar página**  
    > ![Atualizar página][ImageRefreshPage]  

O DevTools amplia automaticamente a parte da gravação na qual a maioria da atividade ocorreu.  

> ##### Figura 3  
> Uma gravação de carregamento de página  
> ![Uma gravação de carregamento de página][ImageLoadRecording]  

### Capturar capturas de tela durante a gravação   

Habilite a caixa de seleção **capturas** de tela para capturar uma captura de tela de cada quadro durante a gravação.  

> ##### Figura 4  
> A caixa de seleção **capturas de tela**  
> ![A caixa de seleção capturas de tela][ImageScreenshots]  

Consulte [exibir uma captura de tela](#view-a-screenshot) para aprender a interagir com capturas de tela.  

### Forçar coleta de lixo durante a gravação   

Enquanto estiver gravando uma página, clique em **coletar** lixo ![ coletar lixo ][ImageCollectGarbageIcon] para forçar a coleta de lixo.  

> ##### Figura 5  
> Coletar lixo  
> ![Coletar lixo][ImageCollectGarbage]  

### Mostrar configurações de gravação   

Clique em **capturar** configurações ![ de captura de configurações ][ImageCaptureSettingsIcon] para expor mais configurações relacionadas à maneira como o devtools captura gravações de desempenho.  

> ##### Figura 6  
> A seção **configurações de captura**  
> ![A seção Configurações de captura][ImageCaptureSettings]  

### Desabilitar exemplos de JavaScript   

Por padrão, a seção **principal** de uma gravação exibe pilhas de chamadas detalhadas de funções JavaScript que foram chamadas durante a gravação.  Para desativar essas pilhas de chamadas:  

1.  Abrir o menu **configurações de captura** .  Consulte [Mostrar configurações de gravação](#show-recording-settings).  
1.  Habilite a caixa de seleção **desativar exemplos de JavaScript** .  
1.  Faça uma gravação da página.  

As [figuras 7](#figure-7) e [8](#figure-8) mostram a diferença entre desabilitar e habilitar exemplos de JavaScript.  A seção **principal** da gravação é muito mais curta quando a amostragem está desativada, pois ela omite todas as pilhas de chamadas JavaScript.  

> ##### Figura 7  
> Um exemplo de uma gravação quando exemplos de JS está desabilitado  
> ![Um exemplo de uma gravação quando exemplos de JS está desabilitado][ImageJSSamplesDisabled]  

> ##### Figura 8  
> Um exemplo de uma gravação quando exemplos de JS está habilitado  
> ![Um exemplo de uma gravação quando exemplos de JS está habilitado][ImageJSSamplesEnabled]  

### Acelerar a rede durante a gravação   

Para acelerar a rede durante a gravação:  

1.  Abrir o menu **configurações de captura** .  Consulte [Mostrar configurações de gravação](#show-recording-settings).  
1.  Defina a **rede** para o nível de limitação desejado.  

### Acelerar a CPU durante a gravação   

Para reduzir a CPU durante a gravação:  

1.  Abrir o menu **configurações de captura** .  Consulte [Mostrar configurações de gravação](#show-recording-settings).  
1.  Defina a **CPU** para o nível de limitação desejado.  

A limitação é relativa às funcionalidades do seu computador.  Por exemplo, a opção **2x de lentidão** faz com que a CPU opere 2 vezes mais lenta do que o normal.  O DevTools não simula realmente as CPUs de dispositivos móveis, porque a arquitetura de dispositivos móveis é muito diferente da dos desktops e laptops.  

### Habilitar a instrumentação avançada de pintura   

Para ver a instrumentação de pintura detalhada:  

1.  Abrir o menu **configurações de captura** .  Consulte [Mostrar configurações de gravação](#show-recording-settings).  
1.  Marque a caixa de seleção **habilitar instrumentação avançada de pintura (lento)** .  

Para saber como interagir com as informações de pintura, consulte [Exibir camadas](#view-layers-information) e [Exibir o criador de perfil de tinta](#view-paint-profiler).  

## Salvar uma gravação   

Para salvar uma gravação, clique com o botão direito do mouse e selecione **salvar perfil**.  

> ##### Figura 9  
> **Salvar perfil**  
> ![Salvar perfil][ImageSaveProfile]  

## Carregar uma gravação   

Para carregar uma gravação, clique com o botão direito do mouse e selecione **carregar perfil**.  

> ##### Figura 10  
> **Carregar perfil**  
> ![Carregar perfil][ImageLoadProfile]  

## Limpar a gravação anterior   

Depois de fazer uma gravação, pressione **limpar** gravação ![ limpar gravação ][ImageClearRecordingIcon] para limpar a gravação do painel **desempenho** .  

> ##### Figura 11  
> Limpar gravação  
> ![Limpar gravação][ImageClearRecording]  

## Analisar uma gravação de desempenho   

Depois de [registrar o desempenho do tempo de execução](#record-runtime-performance) ou o [desempenho da carga de registro](#record-load-performance), o painel **desempenho** fornece muitos dados para analisar o desempenho do que acabou de acontecer.  

### Selecionar uma parte de uma gravação   

Arraste o mouse para a esquerda ou para a direita na **visão geral** para selecionar uma parte de uma gravação.  A **visão geral** é a seção que contém os gráficos de **FPS**, **CPU**e **net** .  

> ##### Figura 12  
> Arrastando o mouse pela visão geral para aplicar zoom  
> ![Arrastando o mouse pela visão geral para aplicar zoom][ImageZoom]  

Para selecionar uma parte usando o teclado:  

1.  Clique no plano de fundo da seção **principal** ou de qualquer uma das seções ao lado dela, como **interações**, **rede**ou **GPU**.  Este fluxo de trabalho de teclado funciona apenas quando uma dessas seções está em foco.  
1.  Use as `W` teclas,, `A` `S` , `D` para ampliar, mover para a esquerda, reduzir e mover para a direita, respectivamente.  

Para selecionar uma parte usando uma trackpad:  

1.  Passe o mouse sobre a seção **visão geral** ou a seção **detalhes** .  A seção **visão geral** é a área que contém os gráficos de **FPS**, **CPU**e **net** .  A seção **detalhes** é a área que contém a seção **principal** , a seção **interações** e assim por diante.  
1.  Usando dois dedos, passe o dedo para baixo para reduzir, deslize o dedo para a esquerda para mover para a esquerda, passe o dedo para baixo para ampliar e passe o dedo para a direita para mover para a direita.  

Para rolar um gráfico de chama longa na seção **principal** ou em qualquer um dos vizinhos, clique e mantenha pressionado enquanto arrasta para cima e para baixo.  Arraste para a esquerda e para a direita para mover qual parte da gravação está selecionada.  

### Atividades de pesquisa   

Pressione `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \) para abrir a caixa de pesquisa na parte inferior do painel **desempenho** .  

> ##### Figura 13  
> Usando Regex na caixa de pesquisa na parte inferior da janela para localizar qualquer atividade que comece com `E`  
> ![A caixa de pesquisa][ImageSearch]  

Para navegar entre atividades que correspondam à sua consulta:  

*   Usar os **Previous** ![ botões anterior ][ImagePreviousIcon] e **próximo** ![ próximo ][ImageNextIcon] .  
*   Pressione `Shift` + `Enter` para selecionar o anterior ou `Enter` para selecionar o próximo.  

Para modificar as configurações de consulta:  

*   Pressione maiúsculas e minúsculas **diferenciando** maiúsculas de minúsculas ![ ][ImageSearchCaseIcon] para fazer a consulta diferencia maiúsculas  
*   Pressione **Regex** ![ Regex Regex ][ImageSearchRegexIcon] para usar uma expressão regular em sua consulta.  

Para ocultar a caixa de pesquisa, clique em **Cancelar**.  

### Exibir atividade de thread principal   

Use a seção **principal** para exibir atividades ocorridas no thread principal da página.  

> ##### Figura 14  
> A seção **principal**  
> ![A seção principal][ImageMain]  

Clique em um evento para ver mais informações sobre ele na guia **Resumo** .  DevTools descreve o evento selecionado.  

> ##### Figura 15  
> Mais informações sobre a `anonymous` função na guia **Resumo**  
> ![Mais informações sobre a função anônimo na guia Resumo][ImageMainEventSummary]  

DevTools representa a atividade de thread principal com um gráfico de chama.  O eixo x representa a gravação ao longo do tempo.  O eixo y representa a pilha de chamadas.  Os eventos na parte superior causam os eventos abaixo dele.  

> ##### Figura 16  
> Um gráfico de chama na seção **principal**  
> ![Um gráfico de chama][ImageFlameChart]  

Na [Figura 16](#figure-16), um `click` evento causou uma `Function Call` entrada na `activitytabs.js` linha 53.  Abaixo `Function Call` , você verá que uma função anônima foi chamada.  A função anônima chamada `a` , que é chamada `wait` , que é chamada `Minor GC` .  

DevTools atribui as cores aleatórias de scripts.  Na [Figura 16](#figure-16), as chamadas de função de um script são verde claro em cores.  As chamadas de outro script são coloridas bege.  O amarelo mais escuro representa a atividade de script e o evento roxo representa a atividade de renderização.  Esses eventos amarelos e roxos mais escuros são consistentes em todas as gravações.  

Confira [desabilitar exemplos de JavaScript](#disable-javascript-samples) se você quiser ocultar o gráfico de chama detalhado de chamadas JavaScript.  Quando os exemplos de JS estiverem desativados, você verá eventos de alto nível, como `Event: click` e `Function Call` da [Figura 16](#figure-16).  

### Exibir atividades em uma tabela   

Depois de gravar uma página, você não precisa confiar exclusivamente na seção **principal** para analisar atividades.  O DevTools também fornece três exibições em tabelas para analisar atividades.  Cada modo de exibição oferece uma perspectiva diferente nas atividades:  

*   Quando quiser exibir as atividades raiz que causam mais trabalho, use [a guia árvore de **chamadas** ](#the-call-tree-tab).  
*   Quando você quiser exibir as atividades nas quais o tempo foi gasto diretamente, use [a guia de **baixo para cima** ](#the-bottom-up-tab).  
*   Quando quiser exibir as atividades na ordem em que elas ocorreram durante a gravação, use [a guia **log de eventos** ](#the-event-log-tab).  

> [!NOTE]
> Todas as próximas três seções fazem referência à mesma demonstração.  Execute a demonstração você mesmo na [demonstração das guias de atividades][ActivityTabsDemo].  

#### Atividades raiz   

Aqui está uma explicação do conceito de **atividades raiz** que é mencionado na guia de **árvore de chamadas** , na guia **de baixo para cima** e nas seções do log de **eventos** .  

As atividades raiz são aquelas que fazem com que o navegador execute algum trabalho.  Por exemplo, quando você clica em uma página, o navegador dispara uma `Event` atividade como a atividade raiz.  Isso `Event` pode fazer com que um manipulador seja executado e assim por diante.  

No gráfico chama da seção **principal** , as atividades raiz estão na parte superior do gráfico.  Nas guias **árvore de chamadas** e **log de eventos** , as atividades raiz são os itens de nível superior.  

Consulte [a guia árvore de chamadas](#the-call-tree-tab) para obter um exemplo de atividades de raiz.  

#### A guia árvore de chamadas   

Use a guia **árvore de chamadas** para ver quais [atividades raiz](#root-activities) causam mais trabalho.  

A guia **árvore de chamadas** exibe apenas atividades durante a parte selecionada da gravação.  Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.  

> ##### Figura 17  
> A guia **árvore de chamadas**  
> ![A guia árvore de chamadas][ImageCallTree]  

Na [Figura 17](#figure-17), o nível superior de itens na coluna **atividade** , como `Evaluate Script` e `Parse HTML` são atividades raiz.  O aninhamento representa a pilha de chamadas.  Por exemplo, na [Figura 17](#figure-17), `Parse HTML` que causou `Evaluate Script` o resultado `Compile Script` e `(anonymous)` .  

A **auto-tempo** representa o tempo gasto diretamente nessa atividade.  **Tempo total** representa o tempo gasto nessa atividade ou em qualquer um dos filhos.  

Clique em **período automático**, **tempo total**ou **atividade** para classificar a tabela por essa coluna.  

Use a caixa de texto **Filtrar** para filtrar eventos por nome da atividade.  

Por padrão, o menu **agrupamento** é definido como **sem agrupamento**.  Use o menu **agrupamento** para classificar a tabela de atividades com base em vários critérios.  

Clique em **Mostrar pilha mais pesada** ![ Mostrar pilha mais pesada ][ImageShowHeaviestStackIcon] para revelar outra tabela à direita da tabela **atividade** .  Clique em uma atividade para preencher a tabela de **pilha mais pesada** .  A tabela de **pilha mais pesada** mostra quais filhos da atividade selecionada levaram o tempo mais longo para ser executado.  

#### A guia seta para baixo   

Use a guia de **cima para baixo** para ver quais atividades resumiram diretamente na maior parte do tempo em agregação.  

A guia de **cima para baixo** exibe apenas atividades durante a parte selecionada da gravação.  Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.  

> ##### Figura 18  
> A guia **seta para baixo**  
> ![A guia seta para baixo][ImageBottomUp]  

Na seção **principal** , gráfico da [Figura 18](#figure-18), veja que quase todo o tempo gastou em execução `Parse HTML` .  A atividade superior na guia de **baixo para cima** da [Figura 18](#figure-18) é `Parse HTML` .  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Veja na guia **abaixo** , a próxima atividade mais cara é `Layout` .  

A coluna **auto-time** representa o tempo agregado gasto diretamente nessa atividade em todas as ocorrências.  

A coluna **tempo total** representa o tempo agregado gasto na atividade ou em qualquer um dos filhos.  

#### A guia log de eventos   

Use a guia **log de eventos** para exibir atividades na ordem em que elas ocorreram durante a gravação.  

A guia **log de eventos** exibe apenas as atividades durante a parte selecionada da gravação.  Consulte [selecionar uma parte de uma gravação](#select-a-portion-of-a-recording) para aprender a selecionar partes.  

> ##### Figura 19  
> A guia **log de eventos**  
> ![A guia log de eventos][ImageEventLog]  

A coluna **hora de início** representa o ponto em que a atividade começou, em relação ao início da gravação.  Por exemplo, a hora de início do `175.7 ms` item selecionado na [Figura 19](#figure-19) significa que a atividade começou 175,7 MS após o início da gravação.  

A coluna **auto-time** representa o tempo gasto diretamente nessa atividade.  

As colunas de **tempo total** representam o tempo gasto diretamente nessa atividade ou em qualquer um dos filhos.  

Clique em **hora de início**, **hora automática**ou **tempo total** para classificar a tabela por essa coluna.

Use a caixa de texto **Filtrar** para filtrar atividades por nome.  

Use o menu **duração** para filtrar todas as atividades que levaram menos de 1 MS ou 15 ms.  Por padrão, o menu **duração** é definido como **todos**, o que significa que todas as atividades são mostradas.  

Desative as caixas de seleção **carregar**, **script**, **renderização**ou **pintura** para filtrar todas as atividades dessas categorias.  

### Exibir atividade GPU   

Exiba a atividade GPU na seção **GPU** .  

> ##### Figura 20  
> A seção **GPU**  
> ![A seção GPU][ImageGpu]  

### Exibir atividade rasterizada   

Exiba atividades rasterizadas na seção de **rasterização** .  

> ##### Figura 21  
> A seção de **rasterização**  
> ![A seção de rasterização][ImageRaster]  

### Exibir interações   

Use a seção **interações** para localizar e analisar interações do usuário ocorridas durante a gravação.  

> ##### Figura 22  
> A seção **interações**  
> ![A seção interações][ImageInteractions]  

Uma linha vermelha na parte inferior de uma interação representa o tempo gasto aguardando o thread principal.  

Clique em uma interação para ver mais informações sobre ela na guia **Resumo** .  

### Analisar quadros por segundo (FPS)   

O DevTools oferece várias maneiras de analisar os quadros por segundo:  

*   Use [o gráfico de **FPS** ](#the-fps-chart) para obter uma visão geral de FPS na duração da gravação.  
*   Use [a seção **quadros** ](#the-frames-section) para ver quanto tempo um determinado quadro levou.  
*   Use o **medidor de FPS** para uma estimativa em tempo real de FPS à medida que a página é executada.  Consulte [exibir quadros por segundo em tempo real com o medidor de FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).  

#### O gráfico de FPS   

O gráfico de **FPS** fornece uma visão geral da taxa de quadros na duração de uma gravação.  Em geral, quanto maior a barra verde, melhor a taxa de quadros.  

Uma barra vermelha acima do gráfico de **FPS** é um aviso informando que a taxa de quadros ficou tão baixa que provavelmente danificaram a experiência do usuário.  

> ##### Figura 23  
> O gráfico de FPS  
> ![O gráfico de FPS][ImageFpsChart]  

#### A seção quadros   

A seção **frames** informa exatamente quanto tempo um determinado quadro levou.  

Passe o mouse sobre um quadro para exibir uma dica de ferramenta com mais informações sobre ele.  

> ##### Figura 24  
> Passar o mouse sobre um quadro  
> ![Passar o mouse sobre um quadro][ImageFramesSection]  

Clique em um quadro para ver ainda mais informações sobre o quadro na guia **Resumo** .  DevTools descreve o quadro selecionado em azul.  

> ##### Figura 25  
> Exibir um quadro na guia **Resumo**  
> ![Exibir um quadro na guia Resumo][ImageFrameSummary]  

### Exibir solicitações de rede   

Expanda a seção **rede** para ver a cascata de solicitações de rede ocorridas durante a gravação.  

> ##### Figura 26  
> A seção **rede**  
> ![A seção rede][ImageNetworkRequest]  

As solicitações são codificadas por cor da seguinte maneira:  

*   HTML: azul  
*   CSS: roxo  
*   JS: amarelo  
*   Imagens: verde  

Clique em uma solicitação para ver mais informações sobre ela na guia **Resumo** .  Por exemplo, na [Figura 26](#figure-26) , a guia **Resumo** está exibindo mais informações sobre a solicitação azul selecionada na seção **rede** .  

Um quadrado mais escuro-azul no canto superior esquerdo de uma solicitação significa que é uma solicitação de prioridade mais alta.  Um quadrado azul mais claro significa prioridade mais baixa.  Por exemplo, na [Figura 26](#figure-26) , a solicitação azul selecionada é de prioridade mais alta, e a verde abaixo é de prioridade mais baixa.  

Na [Figura 27](#figure-27), a solicitação para `www.bing.com` é representada por uma linha à esquerda, uma barra no meio com uma parte escura e uma parte Light e uma linha à direita.  A [Figura 28](#figure-28) mostra a representação correspondente da mesma solicitação na guia **intervalo** do painel **rede** .  Veja como essas duas representações são mapeadas umas com as outras:

*   A linha à esquerda está tudo no `Connection Start` grupo de eventos, inclusive.  Em outras palavras, ele é tudo antes `Request Sent` , exclusivo.  
*   A parte leve da barra é `Request Sent` e `Waiting (TTFB)` .  
*   A parte escura da barra está `Content Download` .  
*   A linha certa é essencialmente tempo gasto aguardando o thread principal.  Isso não é representado na guia **intervalo** .  

> ##### Figura 27  
> A representação de barra de linhas da `www.bing.com` solicitação  
> ![A representação de barra de linhas da solicitação www.bing.com][ImageLineBar]  

> ##### Figura 28  
> A representação da guia **intervalo** da `www.bing.com` solicitação  
> ![A seção rede][ImageTiming]  

### Exibir métricas de memória   

Habilite a caixa de seleção **memória** para exibir as métricas de memória da última gravação.  

> ##### Figura 29  
> A caixa de seleção **memória**  
> ![A caixa de seleção memória][ImageMemory]  

O DevTools exibe um novo gráfico de **memória** , acima da guia **Resumo** .  Há também um novo gráfico abaixo do gráfico de **rede** , chamado **heap**.  O gráfico de **heap** fornece as mesmas informações que a linha de **heap do js** no gráfico de **memória** .  

> ##### Figura 30  
> Métricas de memória, acima da guia **Resumo**  
> ![Métricas de memória][ImageMemoryMetrics]  

As linhas coloridas do gráfico são mapeadas para as caixas de seleção coloridas acima do gráfico.  
Desative uma caixa de seleção para ocultar essa categoria do gráfico.  

O gráfico só exibe a região da gravação selecionada no momento.  Por exemplo, na [Figura 30](#figure-30), o gráfico de **memória** só mostra o uso da memória em torno da 400 ms Mark para a 1750 MS Mark.  

### Exibir a duração de uma parte de uma gravação   

Ao analisar uma seção como **Network** ou **Main**, às vezes você precisa de uma estimativa mais precisa de tempo que determinados eventos levaram.  Segure `Shift` , clique e segure e arraste para a esquerda ou para a direita para selecionar uma parte da gravação.  Na parte inferior da seleção, o DevTools mostra o tempo que a parte levou.  

> ##### Figura 31  
> O `9.47ms` carimbo de data/hora na parte inferior da parte selecionada indica o tempo que a parte levou  
> ![Exibindo a duração de uma parte de uma gravação][ImageDuration]  

### Exibir uma captura de tela   

Consulte [capturar capturas de tela durante a gravação](#capture-screenshots-while-recording) para saber como habilitar capturas de tela.  

Passe o mouse sobre a **visão geral** para ver uma captura de tela de como a página procurou durante a gravação.  A **visão geral** é a seção que contém os gráficos **CPU**, **FPS**e **net** .  

> ##### Figura 32  
> Visualizando uma captura de tela  
> ![Visualizando uma captura de tela][ImageViewScreenshot]  

Você também pode exibir capturas de tela clicando em um quadro na seção **quadros** .  O DevTools exibe uma versão pequena da captura de tela na guia **Resumo** .  

> ##### Figura 33  
> Depois de clicar no `233.9ms` quadro na seção **quadros** , a captura de tela desse quadro é exibida na guia **Resumo**  
> ![Exibir uma captura de tela na guia Resumo][ImageFrameScreenshotSummary]  

Clique na miniatura na guia **Resumo** para ampliar a captura de tela.  

> ##### Figura 34  
> Depois de clicar na miniatura na guia **Resumo** , o devtools amplia a captura de tela  
> ![Ampliando uma captura de tela na guia Resumo][ImageFrameScreenshotZoom]  

### Exibir informações de camadas   

Para exibir as informações de camadas avançadas sobre um quadro:  

1.  [Habilite a instrumentação avançada de pintura](#enable-advanced-paint-instrumentation).  
1.  Selecione um quadro na seção **quadros** .  DevTools exibe informações sobre as camadas na guia novas **camadas** , ao lado da guia **log de eventos** .  
    
    > ##### Figura 35  
    > O painel **camadas**  
    > ![O painel camadas][ImageLayers]  
    
Passe o mouse sobre uma camada para realçá-la no diagrama.  

> ##### Figura 36  
> Realçando **#39** de camada  
> ![Realçando uma camada][ImageLayerHover]  

Para mover o diagrama:  

*   Clique **em modo panorâmico panorâmico** ![ ][ImagePanModeIcon] para mover-se pelos eixos X e Y.  
*   Clique **em modo de rotação** ![ do modo de rotação ][ImageRotateModeIcon] para girar ao longo do eixo Z.  
*   Clique em **Redefinir transformação** ![ Redefinir transformação ][ImageResetTransformIcon] para redefinir o diagrama para a posição original.  

### Exibir o gerador de perfil do Paint   

Para exibir informações avançadas sobre um evento de pintura:  

1.  [Habilite a instrumentação avançada de pintura](#enable-advanced-paint-instrumentation).  
1.  Selecione um evento de **pintura** na seção **principal** .  
    
    > ##### Figura 37  
    > A guia **perfil do Paint**  
    > ![A guia perfil do Paint][ImagePaintProfiler]  
    
## Analisar o desempenho de renderização com a guia renderização   

Use os recursos da guia **renderização** para ajudar a visualizar o desempenho de renderização da página.  

Para abrir a guia **renderização** :  

1.  [Abrir o menu de comandos][DevToolsCommandMenu].  
1.  Comece a digitar `Rendering` e selecione `Show Rendering` .  DevTools exibe a guia **renderização** na parte inferior da janela do devtools.  
    
    > ##### Figura 38  
    > A guia **renderização**  
    > ![A guia renderização][ImageRenderingTab]  
    
### Exibir quadros por segundo em tempo real com o medidor de FPS   

O **medidor de FPS** é uma sobreposição que aparece no canto superior direito do seu visor.  Ele fornece uma estimativa em tempo real de FPS à medida que a página é executada.  Para abrir o **medidor de FPS**:  

1.  Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Habilitar a caixa de seleção **meter de FPS** .  
    
    > ##### Figura 39  
    > O medidor de FPS  
    > ![O medidor de FPS][ImageFpsMeter]  
    
### Exibir eventos de pintura em tempo real com o Paint piscando   

Use o Paint para obter uma exibição em tempo real de todos os eventos de pintura na página.  Sempre que uma parte da página é pintada novamente, o DevTools descreve essa seção em verde.  

Para habilitar a intermitência de tinta:  

1.  Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Habilitar a caixa de seleção **pintura em intermitência** .  
    
    > ##### Figura 40  
    > **Pintura em intermitência**  
    > ![Pintura em intermitência][ImagePaintFlashing]  
    
### Exibir uma sobreposição de camadas com bordas de camada   

Use **bordas de camada** para exibir uma sobreposição de bordas de camada e blocos na parte superior da página.  

Para habilitar bordas de camada:  

1.  Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Habilitar a caixa de seleção **bordas de camada** .  
    
    > ##### Figura 41  
    > **Bordas de camada**  
    > ![Bordas de camada][ImageLayerBorders]  
    
Veja os comentários em [`debug_colors.cc`][ChromiumDebugColors] para obter uma explicação das codificações de cores.  

### Encontrar problemas de desempenho de rolagem em tempo real   

Use problemas de desempenho de rolagem para identificar elementos da página que têm ouvintes de eventos relacionados a rolagem que podem danificar o desempenho da página.  
DevTools descreve os elementos que podem ser problemáticos em azul-petróleo.  

Para ver os problemas de desempenho de rolagem:  

1.  Abrir a guia **renderização** .  Consulte [analisar o desempenho de renderização com a guia renderização](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Habilitar a caixa de seleção de **problemas de desempenho de rolagem** .  
 
    > ##### Figura 42  
    > Os **problemas de desempenho de rolagem** indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem  
    > ![Os problemas de desempenho de rolagem indicam que os objetos restritos de não-camada podem danificar o desempenho de rolagem][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Figura 1: gravar"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Figura 2: página de atualização"  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Figura 3: uma gravação de carregamento de página"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Figura 4: caixa de seleção capturas de tela"  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Figura 5: coletar lixo"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Figura 6: seção de configurações de captura"  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Figura 7: um exemplo de uma gravação quando exemplos de JS são desabilitados"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Figura 8: um exemplo de uma gravação quando os exemplos de JS estão habilitados"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Figura 9: salvar perfil"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Figura 10: carregar perfil"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Figura 11: limpar a gravação"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Figura 12: arrastando o mouse pela visão geral para aplicar zoom"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Figura 13: caixa de pesquisa"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figura 14: seção principal"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Figura 15: mais informações sobre a função anônimo na guia Resumo"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Figura 16: um gráfico de chama"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Figura 17: guia da árvore de chamadas"  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Figura 18: a guia de baixo para cima"  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Figura 19: a guia log de eventos"  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Figura 20: seção GPU"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Figura 21: a seção de rasterização"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Figura 22: seção interações"  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Figura 23: o gráfico de FPS"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Figura 24: passando o mouse sobre um quadro"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Figura 25: exibindo um quadro na guia Resumo"  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Figura 26: seção rede"  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Figura 27: representação de barra de linhas da solicitação www.bing.com"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Figura 28: seção Network"  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Figura 29: a caixa de seleção memória"  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Figura 30: métricas de memória"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Figura 31: exibindo a duração de uma parte de uma gravação"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Figura 32: exibindo uma captura de tela"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Figura 33: exibindo uma captura de tela na guia Resumo"  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Figura 34: ampliando uma captura de tela na guia Resumo"  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Figura 35: o painel camadas"  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Figura 36: realçando uma camada"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Figura 37: a guia do criador de perfil do Paint"  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Figura 38: a guia renderização"  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Figura 39: o medidor de FPS"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Figura 40: pintura em intermitência"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Figura 41: bordas da camada"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Figura 42: problemas de desempenho de rolagem indica que os objetos que não se enlimitadas de viewport-Layer podem danificar o desempenho de rolagem"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Abrir o menu de comandos-executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Comece a analisar o desempenho do tempo de execução"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demonstração de guias de atividades"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. CC-pesquisa de código"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
